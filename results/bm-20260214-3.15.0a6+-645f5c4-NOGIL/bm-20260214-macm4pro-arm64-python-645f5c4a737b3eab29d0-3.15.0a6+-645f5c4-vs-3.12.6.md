# Results vs. 3.12.6

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.102x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| tomli_loads          | 957 ms                                                   | 870 ms: 1.10x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.00x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.73 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.46 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 788 us: 2.55x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 241 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 503 us: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 789 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.8 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 53.9 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 870 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.87 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 456 ms: 1.09x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.6 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.5 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.0 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 659 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.00x faster                                                    |
| nbody                            | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.8 us: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.1 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.1 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.1 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.97 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.4 ms: 1.14x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.46 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                     |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.6 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.73 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.13 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 548 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 266 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.4 ms: 1.43x slower                                                    |
| connected_components             | 201 ms                                                   | 303 ms: 1.51x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): json, sympy_integrate, dask, scimark_monte_carlo
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-NOGIL/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.36x