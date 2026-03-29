# Results vs. 3.12.6

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.173x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 20.9 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.9 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.1 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.7 ms: 1.16x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.0 ms: 1.24x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.82 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| tomli_loads          | 957 ms                                                   | 759 ms: 1.26x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.2 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.3 us: 1.10x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.61 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.15 ms: 1.15x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.9 ms: 1.09x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.93 ms: 5.29x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.9 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| deepcopy                         | 161 us                                                   | 95.1 us: 1.70x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.61x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.9 ms: 1.47x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.00 us: 1.41x faster                                                    |
| go                               | 70.0 ms                                                  | 51.4 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.3 ns: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 42.7 ms: 1.27x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 759 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 891 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.0 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.6 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.7 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.15 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.5 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.9 us: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.2 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 93.3 us: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.9 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.3 ms: 1.10x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.9 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 622 ms: 1.07x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.9 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.9 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 942 ns: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 411 us: 1.02x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                     |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.3 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.82 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.61 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 937 us: 1.13x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.7 ms: 1.18x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.43 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.1 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (2): fannkuch, sympy_expand
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea-CLANG/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.173x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.22x