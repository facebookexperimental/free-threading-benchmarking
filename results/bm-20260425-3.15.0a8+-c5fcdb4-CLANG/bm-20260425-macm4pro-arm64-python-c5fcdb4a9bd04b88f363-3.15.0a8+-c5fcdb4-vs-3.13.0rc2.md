# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 218 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.2 ms: 1.44x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.0 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.9 ms: 1.09x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 770 ms: 1.30x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.3 ms: 1.08x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.3 us: 1.07x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.83 ms: 1.02x faster                                                    |
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 19.9 ms: 1.07x faster                                                    |
| mako            | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 218 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| pylint                           | 106 ms                                                         | 49.9 ms: 2.12x faster                                                    |
| mdp                              | 1.06 sec                                                       | 522 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.93 ms: 1.60x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.0 us: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.44x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.2 ms: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 51.8 ms: 1.40x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 48.0 ms: 1.33x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 770 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.69 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 43.9 ms: 1.09x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.93 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.08x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 33.3 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.9 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 93.3 us: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| generators                       | 15.7 ms                                                        | 15.0 ms: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 311 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 960 us: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 631 ms: 1.03x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.31 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 36.2 ms: 1.03x faster                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 5.83 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.9 ns: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.6 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.01x faster                                                     |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| bench_thread_pool                | 412 us                                                         | 413 us: 1.00x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.94 us: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.7 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 44.6 ms: 1.04x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.0 ms: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.87 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.98 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.7 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.50 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (2): shortest_path, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4-CLANG/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x