# Results vs. 3.12.6

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.100x faster
- HPT reliability: 99.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.5 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| tomli_loads          | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.13 ms: 5.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 795 us: 2.53x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 501 us: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 796 ns: 1.21x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.1 ms: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.38 us: 1.17x faster                                                    |
| go                               | 70.0 ms                                                  | 59.9 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 854 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.7 ms: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.8 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.18 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 670 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.6 us: 1.02x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.1 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| thrift                           | 322 us                                                   | 343 us: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.5 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.56 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.6 ms: 1.17x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 574 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.5 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (3): html5lib, pprint_safe_repr, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea-NOGIL/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 99.55% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.37x