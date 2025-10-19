# Results vs. 3.13.0rc2

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 237 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.9 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.53 ms: 1.05x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 775 ms: 1.29x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 89.5 us: 1.11x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.7 ms: 1.09x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.5 ms: 1.08x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.01 ms: 1.11x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                    |
| mako            | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 237 ms: 2.22x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                     |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.0 us: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 983 ms: 1.49x faster                                                     |
| go                               | 72.6 ms                                                        | 50.2 ms: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 775 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.28x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.70 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.2 ms: 1.25x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.17x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.1 ms: 1.16x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.6 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.56 ms: 1.11x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 89.5 us: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.0 ms: 1.11x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.01 ms: 1.11x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.78 ms: 1.10x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 904 us: 1.10x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 32.7 ms: 1.09x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.09x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.4 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.5 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.95 ms: 1.08x faster                                                    |
| thrift                           | 309 us                                                         | 289 us: 1.07x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 60.9 us: 1.06x faster                                                    |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.12 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.05x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.53 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.35 us: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 39.1 ns: 1.04x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| bench_thread_pool                | 412 us                                                         | 398 us: 1.03x faster                                                     |
| 2to3                             | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 457 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                    |
| sympy_expand                     | 159 ms                                                         | 156 ms: 1.02x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                     |
| sympy_str                        | 95.5 ms                                                        | 93.9 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.02x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.98 us: 1.03x slower                                                    |
| pylint                           | 106 ms                                                         | 109 ms: 1.03x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.1 ms: 1.03x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.62 ms: 1.05x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.8 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| many_optionals                   | 200 us                                                         | 354 us: 1.76x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.1 ms: 2.73x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.9 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): meteor_contest, sympy_sum, shortest_path
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-CLANG/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x