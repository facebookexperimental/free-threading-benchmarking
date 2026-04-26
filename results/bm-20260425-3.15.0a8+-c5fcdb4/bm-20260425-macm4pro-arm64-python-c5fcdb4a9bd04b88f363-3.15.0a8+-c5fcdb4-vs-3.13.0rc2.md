# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.081x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.3 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.5 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.6 us: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.96 ms: 1.00x slower                                                    |
| python_startup         | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| pylint                           | 106 ms                                                         | 51.3 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 228 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.01 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.2 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.22x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.9 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 963 us: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 635 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.6 us: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.6 ms: 1.00x faster                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 5.96 ms: 1.00x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.58 ms: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.26 us: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.14 us: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.7 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.2 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.5 ms: 1.07x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 39.0 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.47 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.3 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (5): sqlite_synth, json_loads, pycparser, logging_format, scimark_sparse_mat_mult
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.081x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.20x