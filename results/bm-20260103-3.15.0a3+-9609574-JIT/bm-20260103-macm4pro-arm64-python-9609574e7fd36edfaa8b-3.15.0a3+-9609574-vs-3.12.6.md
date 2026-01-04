# Results vs. 3.12.6

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.250x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.20x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.5 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.8 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.5 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.6 ms: 1.68x faster                                                    |
| nbody          | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.6 ms: 1.35x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 71.7 us: 1.44x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 110 us: 1.27x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                    |
| tomli_loads          | 957 ms                                                   | 772 ms: 1.24x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 21.8 ms: 1.22x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 8.91 ms: 1.18x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.84 ms: 5.40x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.49 ms: 2.36x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.2 ms: 2.26x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.20x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.02x faster                                                     |
| mdp                              | 1.09 sec                                                 | 579 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.5 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.8 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| float                            | 37.9 ms                                                  | 22.6 ms: 1.68x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                    |
| go                               | 70.0 ms                                                  | 42.8 ms: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.18 us: 1.59x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.12 ms: 1.55x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 33.2 ns: 1.53x faster                                                    |
| pyflate                          | 216 ms                                                   | 142 ms: 1.52x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.0 ms: 1.47x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1000 ns: 1.46x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 42.1 ms: 1.45x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 71.7 us: 1.44x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.41x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 36.5 ms: 1.41x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                    |
| raytrace                         | 145 ms                                                   | 105 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| nbody                            | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 250 ms: 1.35x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 40.6 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 40.5 ms: 1.34x faster                                                    |
| chaos                            | 28.9 ms                                                  | 21.9 ms: 1.32x faster                                                    |
| k_core                           | 1.12 sec                                                 | 860 ms: 1.30x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 518 ms: 1.28x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 256 ms: 1.28x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 110 us: 1.27x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 30.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 772 ms: 1.24x faster                                                     |
| mako                             | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 21.8 ms: 1.22x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.10 us: 1.22x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.21x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 37.5 ms: 1.21x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.32 us: 1.21x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 8.91 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.61 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.5 us: 1.14x faster                                                    |
| pycparser                        | 497 ms                                                   | 438 ms: 1.14x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 45.3 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| connected_components             | 201 ms                                                   | 198 ms: 1.02x faster                                                     |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| django_template                  | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 918 us: 1.11x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmark hidden because not significant (3): sqlite_synth, regex_v8, sympy_str
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260103-3.15.0a3+-9609574-JIT/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.250x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.25x