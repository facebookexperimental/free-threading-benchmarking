# Results vs. 3.12.6

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.153x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 230 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.5 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 814 ms: 1.18x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.77 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.00 ms: 5.19x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.21x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 230 ms: 2.08x faster                                                     |
| mdp                              | 1.09 sec                                                 | 539 ms: 2.03x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.9 us: 1.63x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                    |
| float                            | 37.9 ms                                                  | 26.7 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.20 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| go                               | 70.0 ms                                                  | 53.3 ms: 1.31x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                     |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.0 ns: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.7 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.6 ms: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 814 ms: 1.18x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.20 us: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.5 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.17x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 47.0 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.8 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.4 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.7 us: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.4 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.77 ms: 1.07x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.9 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 641 ms: 1.04x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 65.5 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 317 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 314 us: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 951 ns: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.89 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 962 us: 1.16x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.46 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.5 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): crypto_pyaes
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.153x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.24x