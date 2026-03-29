# Results vs. 3.12.6

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.277x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 19.4 ms: 1.19x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 217 ms: 2.21x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 207 ms: 2.16x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 91.2 ms: 1.96x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 90.2 ms: 1.91x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 36.6 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.3 ms: 1.62x faster                                                    |
| nbody          | 54.2 ms                                                  | 33.8 ms: 1.60x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.8 ms: 1.37x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 633 ms: 1.51x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 21.3 ms: 1.26x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 84.0 us: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 31.7 ms: 1.22x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 126 us: 1.11x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 8.89 ms: 1.18x faster                                                    |
| mako            | 4.77 ms                                                  | 4.11 ms: 1.16x faster                                                    |
| django_template | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| Geometric mean  | (ref)                                                    | 1.12x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.57 ms: 5.82x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| richards                         | 22.4 ms                                                  | 9.76 ms: 2.30x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 217 ms: 2.21x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.7 ms: 2.17x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 207 ms: 2.16x faster                                                     |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 91.2 ms: 1.96x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 90.2 ms: 1.91x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 27.8 ms: 1.85x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 34.8 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.3 us: 1.68x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 5.90 us: 1.67x faster                                                    |
| float                            | 37.9 ms                                                  | 23.3 ms: 1.62x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| nbody                            | 54.2 ms                                                  | 33.8 ms: 1.60x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.11 ms: 1.55x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 633 ms: 1.51x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 93.9 ms: 1.51x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 36.3 ms: 1.50x faster                                                    |
| go                               | 70.0 ms                                                  | 47.1 ms: 1.49x faster                                                    |
| pyflate                          | 216 ms                                                   | 146 ms: 1.48x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 34.9 ns: 1.46x faster                                                    |
| logging_format                   | 2.80 us                                                  | 1.93 us: 1.45x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 1.78 us: 1.45x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                    |
| chaos                            | 28.9 ms                                                  | 20.5 ms: 1.41x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.9 ms: 1.41x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 31.6 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 39.8 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 499 ms: 1.33x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 247 ms: 1.33x faster                                                     |
| raytrace                         | 145 ms                                                   | 109 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| k_core                           | 1.12 sec                                                 | 859 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 21.3 ms: 1.26x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.42 ms: 1.25x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.79 sec: 1.25x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 36.6 ms: 1.24x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.69 ms: 1.23x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 84.0 us: 1.22x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 31.7 ms: 1.22x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.8 ms: 1.22x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.4 ms: 1.19x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 8.89 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| fannkuch                         | 176 ms                                                   | 150 ms: 1.17x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.11 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.0 us: 1.13x faster                                                    |
| pycparser                        | 497 ms                                                   | 446 ms: 1.12x faster                                                     |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 126 us: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                    |
| django_template                  | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                    |
| thrift                           | 322 us                                                   | 299 us: 1.08x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.8 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.5 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                     |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.04x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 46.0 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 987 ms: 1.04x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 935 ns: 1.03x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| telco                            | 2.61 ms                                                  | 2.59 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 954 us: 1.15x slower                                                     |
| many_optionals                   | 195 us                                                   | 231 us: 1.18x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.41 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.9 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmark hidden because not significant (2): 2to3, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea-JIT/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.277x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.28x