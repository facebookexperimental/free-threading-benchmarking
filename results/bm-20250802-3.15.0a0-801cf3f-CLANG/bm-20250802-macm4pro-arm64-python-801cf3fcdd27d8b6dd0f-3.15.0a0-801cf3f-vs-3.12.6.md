# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.140x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 396 ms: 1.10x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.60x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.6 ms: 1.18x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.6 ms: 2.63x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.1 ms: 1.24x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate   | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                   |
| tomli_loads          | 957 ms                                                   | 808 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.5 ms: 1.18x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 94.1 us: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.39 ms: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.64 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.11 ms: 1.15x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| mako            | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 521 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.64x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.3 us: 1.63x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.60x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.2 ms: 1.55x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.99 us: 1.41x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                   |
| go                               | 70.0 ms                                                  | 50.7 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                   |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.4 ns: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 16.7 ms: 1.24x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.1 ms: 1.24x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 44.1 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.8 ms: 1.19x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 808 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.5 ms: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 38.6 ms: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.2 ms: 1.17x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.20 us: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 957 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.9 us: 1.17x faster                                                   |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                  |
| richards_super                   | 25.4 ms                                                  | 22.0 ms: 1.16x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.11 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                   |
| thrift                           | 322 us                                                   | 292 us: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 396 ms: 1.10x faster                                                    |
| sympy_str                        | 104 ms                                                   | 95.1 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 94.1 us: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 622 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 472 ms: 1.06x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.54 ms: 1.05x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.2 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                   |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.39 ms: 1.03x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.64 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.19 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 942 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                   |
| many_optionals                   | 195 us                                                   | 306 us: 1.57x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.6 ms: 2.63x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (4): bench_thread_pool, shortest_path, docutils, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250802-3.15.0a0-801cf3f-CLANG/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.140x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.13x