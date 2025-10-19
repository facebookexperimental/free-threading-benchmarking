# Results vs. 3.13.0rc2

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.029x faster
- HPT reliability: 99.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.97x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.66 ms: 1.11x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 829 ms: 1.21x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 92.1 us: 1.08x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.87 ms: 1.01x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 546 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 248 ms: 1.56x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 12.0 us: 1.37x faster                                                    |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 56.1 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 829 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 261 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.70 ms: 1.13x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 578 ms: 1.12x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 288 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.66 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 912 us: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 92.1 us: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.9 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.0 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.8 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.02x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                     |
| sphinx                           | 409 ms                                                         | 403 ms: 1.01x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.87 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.51 ms: 1.00x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 414 us: 1.00x slower                                                     |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.86 ms: 1.03x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 486 ms: 1.03x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.53 us: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.04x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.8 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| shortest_path                    | 225 ms                                                         | 241 ms: 1.07x slower                                                     |
| connected_components             | 208 ms                                                         | 225 ms: 1.08x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.43 us: 1.09x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.8 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 378 us: 1.88x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.84x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.1 ms: 2.97x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (4): mako, logging_silent, gc_traversal, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 99.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x