# Results vs. 3.12.6

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.118x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                   |
| tomli_loads          | 957 ms                                                   | 871 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.3 us: 1.06x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                   |
| mako            | 4.77 ms                                                  | 4.71 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.60x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| deepcopy                         | 161 us                                                   | 103 us: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.22 us: 1.36x faster                                                   |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                   |
| go                               | 70.0 ms                                                  | 53.1 ms: 1.32x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 39.0 ns: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.8 ms: 1.21x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.21x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.1 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                  |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.9 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.3 us: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.27 us: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.49 us: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 871 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.35 ms: 1.09x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.73 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.8 ms: 1.07x faster                                                   |
| sympy_str                        | 104 ms                                                   | 97.4 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.3 us: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.0 ms: 1.05x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 636 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 476 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.71 ms: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.84 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 920 us: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.6 ms: 1.21x slower                                                   |
| many_optionals                   | 195 us                                                   | 370 us: 1.89x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (3): sqlite_synth, fannkuch, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x