# Results vs. 3.12.6

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.287x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.30x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 207 ms: 2.16x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 216 ms: 2.12x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 91.2 ms: 1.95x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 92.9 ms: 1.85x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.2 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 21.1 ms: 1.80x faster                                                    |
| nbody          | 54.2 ms                                                  | 34.4 ms: 1.58x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.41x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.4 ms: 1.35x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 626 ms: 1.53x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 72.2 us: 1.43x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 36.5 ms: 1.41x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 112 us: 1.24x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.56 ms: 1.20x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.97 ms: 1.05x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 8.40 ms: 1.25x faster                                                    |
| mako            | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| django_template | 13.6 ms                                                  | 12.7 ms: 1.08x faster                                                    |
| Geometric mean  | (ref)                                                    | 1.17x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.62 ms: 5.74x faster                                                    |
| pylint                           | 128 ms                                                   | 51.1 ms: 2.51x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.30x faster                                                     |
| richards                         | 22.4 ms                                                  | 10.0 ms: 2.24x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 11.4 ms: 2.22x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 207 ms: 2.16x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 216 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 91.2 ms: 1.95x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 92.9 ms: 1.85x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 33.1 ms: 1.84x faster                                                    |
| float                            | 37.9 ms                                                  | 21.1 ms: 1.80x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 28.9 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                     |
| deepcopy                         | 161 us                                                   | 94.6 us: 1.71x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 5.76 us: 1.71x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 33.9 ms: 1.60x faster                                                    |
| nbody                            | 54.2 ms                                                  | 34.4 ms: 1.58x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 626 ms: 1.53x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 34.2 ns: 1.49x faster                                                    |
| raytrace                         | 145 ms                                                   | 99.8 ms: 1.45x faster                                                    |
| go                               | 70.0 ms                                                  | 48.5 ms: 1.44x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 98.3 ms: 1.44x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.20 ms: 1.44x faster                                                    |
| logging_format                   | 2.80 us                                                  | 1.95 us: 1.43x faster                                                    |
| chaos                            | 28.9 ms                                                  | 20.2 ms: 1.43x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 72.2 us: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.43x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 1.80 us: 1.42x faster                                                    |
| pyflate                          | 216 ms                                                   | 152 ms: 1.42x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.5 ms: 1.41x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 31.5 ms: 1.38x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.4 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 40.4 ms: 1.35x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 251 ms: 1.30x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 515 ms: 1.29x faster                                                     |
| k_core                           | 1.12 sec                                                 | 867 ms: 1.29x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 8.40 ms: 1.25x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 112 us: 1.24x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.81 sec: 1.23x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 37.3 ms: 1.22x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.50 ms: 1.22x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.2 ms: 1.21x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 32.1 ms: 1.21x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.56 ms: 1.20x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 18.9 ms: 1.16x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| django_template                  | 13.6 ms                                                  | 12.7 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.3 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.66 ms: 1.05x faster                                                    |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.04x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 46.3 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 163 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                     |
| telco                            | 2.61 ms                                                  | 2.64 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 5.97 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.76 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 969 us: 1.17x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 47.7 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.46 ms: 1.22x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                             |

Benchmark hidden because not significant (1): connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.287x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.29x