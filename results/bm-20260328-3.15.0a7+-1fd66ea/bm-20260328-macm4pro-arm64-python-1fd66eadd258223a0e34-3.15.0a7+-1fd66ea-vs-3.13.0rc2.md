# Results vs. 3.13.0rc2

- fork: python
- ref: 1fd66eadd258223a0e34
- machine: darwin-arm64
- commit hash: 1fd66ea
- commit date: 2026-03-28
- overall geometric mean: 1.070x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.7 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.5 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| nbody          | 42.5 ms                                                        | 44.5 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 814 ms: 1.23x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.77 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.00 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.9 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| go                               | 72.6 ms                                                        | 53.3 ms: 1.36x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.7 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.7 ms: 1.29x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 814 ms: 1.23x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                     |
| float                            | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.09x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.9 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.6 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 962 us: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.77 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.6 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 317 ms: 1.01x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 641 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.0 ns: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                     |
| thrift                           | 309 us                                                         | 314 us: 1.02x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.89 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.5 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.20 us: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.40 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.9 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.46 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.5 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (6): pycparser, genshi_xml, pidigits, typing_runtime_protocols, scimark_sparse_mat_mult, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260328-3.15.0a7+-1fd66ea/bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7+-1fd66ea.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x