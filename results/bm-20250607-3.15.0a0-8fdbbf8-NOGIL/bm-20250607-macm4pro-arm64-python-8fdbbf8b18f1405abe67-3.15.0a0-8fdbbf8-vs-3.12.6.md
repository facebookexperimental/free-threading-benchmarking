# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.101x faster
- HPT reliability: 99.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 990 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.7 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| tomli_loads          | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.82 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                   |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 772 us: 2.60x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.67 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 562 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.9 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.95 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.0 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.2 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.7 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 990 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.89 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.05 ms: 1.00x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| thrift                           | 322 us                                                   | 326 us: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 59.5 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                   |
| 2to3                             | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.0 ms: 1.08x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.78 us: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 52.6 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.10x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.10 us: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.10x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 378 ms: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 768 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.35 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.82 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.27 ms: 1.25x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.6 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 215 ns: 4.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): json, html5lib
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8-NOGIL/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 99.02% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x