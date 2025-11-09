# Results vs. 3.12.6

- fork: python
- ref: 0ac890bea79d3e0162c8
- machine: darwin-arm64
- commit hash: 0ac890b
- commit date: 2025-11-08
- overall geometric mean: 1.158x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 221 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.7 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.7 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.8 ms: 1.16x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.5 ms: 1.26x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                     |
| regex_effbot   | 1.67 ms                                                  | 1.72 ms: 1.03x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 11.1 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 775 ms: 1.24x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 22.9 ms: 1.17x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 89.1 us: 1.15x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.33 ms: 1.12x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.1 ms: 1.08x faster                                                    |
| mako            | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 218 ms: 2.20x faster                                                     |
| mdp                              | 1.09 sec                                                 | 519 ms: 2.10x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 221 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.7 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.7 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.9 us: 1.67x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.0 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.62x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.2 ms: 1.54x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.87 us: 1.43x faster                                                    |
| go                               | 70.0 ms                                                  | 50.3 ms: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.5 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.6 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 893 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.1 ms: 1.24x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 775 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.3 ms: 1.23x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.23x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.2 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| richards                         | 22.4 ms                                                  | 18.9 ms: 1.19x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.57 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 21.6 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.17x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 43.9 ms: 1.17x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 22.9 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.8 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 89.1 us: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.2 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.8 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.9 us: 1.13x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.33 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| thrift                           | 322 us                                                   | 294 us: 1.09x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.1 ms: 1.08x faster                                                    |
| sympy_str                        | 104 ms                                                   | 96.9 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 621 ms: 1.07x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 399 us: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 162 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 951 ns: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 525 ms: 1.01x faster                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.72 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.03x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.14 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.65 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 923 us: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 11.1 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 344 us: 1.76x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (1): docutils
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251108-3.15.0a1+-0ac890b-CLANG/bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.158x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.20x