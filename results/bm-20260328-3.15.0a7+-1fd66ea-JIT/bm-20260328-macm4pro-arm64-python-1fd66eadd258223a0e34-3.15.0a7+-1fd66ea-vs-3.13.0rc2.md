# Results vs. 3.13.0rc2

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.184x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 19.4 ms: 1.19x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 207 ms: 2.52x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 91.2 ms: 1.56x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 90.2 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 36.6 ms: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                    |
| nbody          | 42.5 ms                                                        | 33.8 ms: 1.26x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.8 ms: 1.20x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.59 ms: 1.12x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 633 ms: 1.58x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 21.3 ms: 1.19x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 84.0 us: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 31.7 ms: 1.13x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 126 us: 1.03x faster                                                     |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 9.97 ms                                                        | 8.89 ms: 1.12x faster                                                    |
| mako           | 4.41 ms                                                        | 4.11 ms: 1.07x faster                                                    |
| genshi_xml     | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 207 ms: 2.52x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.76 ms: 2.26x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.7 ms: 2.11x faster                                                    |
| mdp                              | 1.06 sec                                                       | 523 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 34.8 ms: 1.84x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.57 ms: 1.75x faster                                                    |
| k_core                           | 1.46 sec                                                       | 859 ms: 1.70x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 633 ms: 1.58x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 91.2 ms: 1.56x faster                                                    |
| go                               | 72.6 ms                                                        | 47.1 ms: 1.54x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 27.8 ms: 1.54x faster                                                    |
| pyflate                          | 222 ms                                                         | 146 ms: 1.52x faster                                                     |
| deepcopy                         | 145 us                                                         | 96.3 us: 1.51x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 90.2 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.40x faster                                                     |
| float                            | 31.4 ms                                                        | 23.3 ms: 1.35x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 93.9 ms: 1.32x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.9 ms: 1.31x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 247 ms: 1.30x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.30x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 499 ms: 1.30x faster                                                     |
| logging_format                   | 2.45 us                                                        | 1.93 us: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 1.78 us: 1.26x faster                                                    |
| nbody                            | 42.5 ms                                                        | 33.8 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 36.3 ms: 1.20x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 39.8 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 21.3 ms: 1.19x faster                                                    |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 19.4 ms: 1.19x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.79 sec: 1.19x faster                                                   |
| chaos                            | 24.3 ms                                                        | 20.5 ms: 1.19x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.59 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 84.0 us: 1.18x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 36.6 ms: 1.18x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 31.6 ms: 1.18x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.42 ms: 1.18x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 34.9 ns: 1.17x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 5.90 us: 1.15x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 31.7 ms: 1.13x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 8.89 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.59 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                    |
| mako                             | 4.41 ms                                                        | 4.11 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 31.8 ms: 1.06x faster                                                    |
| pycparser                        | 470 ms                                                         | 446 ms: 1.05x faster                                                     |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.69 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 954 us: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 299 us: 1.03x faster                                                     |
| pickle_pure_python               | 130 us                                                         | 126 us: 1.03x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.0 us: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.00x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 53.8 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.5 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.9 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                     |
| many_optionals                   | 200 us                                                         | 231 us: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.41 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmark hidden because not significant (3): django_template, sympy_integrate, raytrace
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea-JIT/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.184x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x