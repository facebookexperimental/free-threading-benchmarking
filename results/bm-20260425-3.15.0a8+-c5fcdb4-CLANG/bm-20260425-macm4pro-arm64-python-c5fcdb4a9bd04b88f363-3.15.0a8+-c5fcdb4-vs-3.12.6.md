# Results vs. 3.12.6

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: darwin-arm64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.180x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 218 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.2 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.0 ms: 1.18x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.9 ms: 1.24x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.3 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| tomli_loads          | 957 ms                                                   | 770 ms: 1.24x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.3 us: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.02x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.83 ms: 1.02x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.9 ms: 1.09x faster                                                    |
| mako            | 4.77 ms                                                  | 4.87 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.04x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.93 ms: 5.29x faster                                                    |
| pylint                           | 128 ms                                                   | 49.9 ms: 2.57x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 218 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| mdp                              | 1.09 sec                                                 | 522 ms: 2.09x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.2 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.0 us: 1.68x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.60x faster                                                    |
| generators                       | 21.9 ms                                                  | 15.0 ms: 1.46x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.94 us: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.36x faster                                                     |
| go                               | 70.0 ms                                                  | 51.8 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 39.9 ns: 1.28x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.0 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.24x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 770 ms: 1.24x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.9 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.2 ms: 1.20x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.0 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.18x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.6 ms: 1.15x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.1 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 93.3 us: 1.10x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.31 ms: 1.10x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.9 ms: 1.09x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.5 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.6 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.7 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| sympy_str                        | 104 ms                                                   | 98.1 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.06x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 631 ms: 1.05x faster                                                     |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.98 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.3 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 413 us: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.87 ms: 1.02x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 5.83 ms: 1.02x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.7 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.93 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 960 us: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.50 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 249 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260425-3.15.0a8+-c5fcdb4-CLANG/bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.180x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x