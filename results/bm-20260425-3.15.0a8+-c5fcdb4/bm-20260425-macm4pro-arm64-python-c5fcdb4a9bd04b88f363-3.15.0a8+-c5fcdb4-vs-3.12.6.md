# Results vs. 3.12.6

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.165x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.3 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.6 us: 1.05x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.96 ms: 1.04x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.71 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.01 ms: 5.18x faster                                                    |
| pylint                           | 128 ms                                                   | 51.3 ms: 2.50x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.10x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.2 us: 1.63x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.14 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.09 us: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| go                               | 70.0 ms                                                  | 53.4 ms: 1.31x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.6 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.6 ns: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.16x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.26 us: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.2 ms: 1.14x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.08x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.9 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.58 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.6 us: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 635 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 315 ms: 1.04x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.1 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.7 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 943 ns: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.71 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 39.0 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 5.96 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.9 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 963 us: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.47 ms: 1.23x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.3 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.165x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.25x