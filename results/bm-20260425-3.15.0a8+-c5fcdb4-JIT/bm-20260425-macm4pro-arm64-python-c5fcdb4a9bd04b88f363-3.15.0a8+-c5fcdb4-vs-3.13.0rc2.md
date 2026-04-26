# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.194x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 19.2 ms: 1.20x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 207 ms: 2.52x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 216 ms: 1.79x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 91.2 ms: 1.56x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.46x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 92.9 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 11.2 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 21.1 ms: 1.49x faster                                                    |
| nbody          | 42.5 ms                                                        | 34.4 ms: 1.24x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.4 ms: 1.19x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 626 ms: 1.60x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 72.2 us: 1.38x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.56 ms: 1.31x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.5 ms: 1.26x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 21.7 ms: 1.17x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 112 us: 1.16x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.97 ms: 1.00x slower                                                    |
| python_startup         | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 8.40 ms: 1.19x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 18.9 ms: 1.13x faster                                                    |
| mako            | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                    |
| django_template | 12.5 ms                                                        | 12.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.10x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 207 ms: 2.52x faster                                                     |
| richards                         | 22.1 ms                                                        | 10.0 ms: 2.21x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.4 ms: 2.16x faster                                                    |
| pylint                           | 106 ms                                                         | 51.1 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 533 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 209 ms: 1.94x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 33.1 ms: 1.94x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 216 ms: 1.79x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.62 ms: 1.73x faster                                                    |
| k_core                           | 1.46 sec                                                       | 867 ms: 1.69x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 626 ms: 1.60x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 91.2 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 94.6 us: 1.53x faster                                                    |
| go                               | 72.6 ms                                                        | 48.5 ms: 1.50x faster                                                    |
| float                            | 31.4 ms                                                        | 21.1 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.49x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 28.9 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 126 ms: 1.46x faster                                                     |
| pyflate                          | 222 ms                                                         | 152 ms: 1.46x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 92.9 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 130 ms: 1.43x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 72.2 us: 1.38x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.56 ms: 1.31x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 33.9 ms: 1.29x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 251 ms: 1.28x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.4 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.5 ms: 1.26x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 515 ms: 1.26x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 98.3 ms: 1.26x faster                                                    |
| logging_format                   | 2.45 us                                                        | 1.95 us: 1.25x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 1.80 us: 1.24x faster                                                    |
| nbody                            | 42.5 ms                                                        | 34.4 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.20 ms: 1.21x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 19.2 ms: 1.20x faster                                                    |
| chaos                            | 24.3 ms                                                        | 20.2 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 8.40 ms: 1.19x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 34.2 ns: 1.19x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 40.4 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 31.5 ms: 1.18x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 5.76 us: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.81 sec: 1.17x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 21.7 ms: 1.17x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.64 ms: 1.16x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 112 us: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.50 ms: 1.14x faster                                                    |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 18.9 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| mako                             | 4.41 ms                                                        | 4.00 ms: 1.10x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| raytrace                         | 109 ms                                                         | 99.8 ms: 1.09x faster                                                    |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 32.1 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 46.3 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 969 us: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.0 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 5.97 ms: 1.00x slower                                                    |
| django_template                  | 12.5 ms                                                        | 12.7 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.76 ms: 1.02x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.66 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 163 ms: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.1 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.3 ms: 1.04x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.2 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.46 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.7 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmark hidden because not significant (1): thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.194x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x