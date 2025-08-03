# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: darwin-arm64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.12x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.8 us: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.43 ms: 1.08x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.91 ms: 1.06x faster                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 255 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.41x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.30 us: 1.35x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.5 ms: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.5 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| float                            | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.3 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.8 us: 1.11x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 92.8 us: 1.11x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 599 ms: 1.11x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 297 ms: 1.10x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.43 ms: 1.08x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.86 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.91 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.61 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.9 ms: 1.04x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.2 ms: 1.02x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                   |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| connected_components             | 201 ms                                                   | 216 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.92 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 941 us: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 324 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (5): json, genshi_xml, regex_v8, json_dumps, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250802-3.15.0a0-801cf3f-JIT/bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.17x