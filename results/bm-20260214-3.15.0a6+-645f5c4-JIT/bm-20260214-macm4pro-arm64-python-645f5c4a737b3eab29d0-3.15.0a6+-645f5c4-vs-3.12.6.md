# Results vs. 3.12.6

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.264x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                    |
| sphinx         | 434 ms                                                   | 381 ms: 1.14x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 216 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 214 ms: 2.09x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 95.1 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 93.5 ms: 1.84x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.68x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 36.8 ms: 1.24x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.7 ms: 1.60x faster                                                    |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 661 ms: 1.45x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 83.2 us: 1.24x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 124 us: 1.12x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.05x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 4.77 ms                                                  | 3.95 ms: 1.21x faster                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.82 ms: 5.43x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.27 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 212 ms: 2.34x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.1 ms: 2.28x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 216 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 214 ms: 2.09x faster                                                     |
| mdp                              | 1.09 sec                                                 | 572 ms: 1.91x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 95.1 ms: 1.87x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 93.5 ms: 1.84x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 28.6 ms: 1.80x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.3 us: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| deepcopy                         | 161 us                                                   | 92.5 us: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.68x faster                                                     |
| float                            | 37.9 ms                                                  | 23.7 ms: 1.60x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.25 us: 1.58x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 39.0 ms: 1.56x faster                                                    |
| go                               | 70.0 ms                                                  | 46.2 ms: 1.52x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.14 ms: 1.51x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 977 ns: 1.50x faster                                                     |
| pyflate                          | 216 ms                                                   | 148 ms: 1.46x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 35.1 ns: 1.45x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 661 ms: 1.45x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 98.1 ms: 1.45x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.8 ms: 1.41x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 39.3 ms: 1.38x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| raytrace                         | 145 ms                                                   | 110 ms: 1.31x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 508 ms: 1.31x faster                                                     |
| chaos                            | 28.9 ms                                                  | 22.2 ms: 1.30x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 252 ms: 1.30x faster                                                     |
| k_core                           | 1.12 sec                                                 | 859 ms: 1.30x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.25x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 36.8 ms: 1.24x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 83.2 us: 1.24x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.5 ms: 1.23x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 21.7 ms: 1.23x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.82 sec: 1.23x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.10 us: 1.23x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.29 us: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.8 ms: 1.21x faster                                                    |
| mako                             | 4.77 ms                                                  | 3.95 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                    |
| pycparser                        | 497 ms                                                   | 424 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.66 ms: 1.14x faster                                                    |
| fannkuch                         | 176 ms                                                   | 154 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| sphinx                           | 434 ms                                                   | 381 ms: 1.14x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 124 us: 1.12x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.8 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                     |
| meteor_contest                   | 47.7 ms                                                  | 44.5 ms: 1.07x faster                                                    |
| json                             | 1.93 ms                                                  | 1.80 ms: 1.07x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 214 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                    |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 888 us: 1.07x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.6 ms: 1.21x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmark hidden because not significant (2): django_template, gc_traversal
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-JIT/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.264x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.27x