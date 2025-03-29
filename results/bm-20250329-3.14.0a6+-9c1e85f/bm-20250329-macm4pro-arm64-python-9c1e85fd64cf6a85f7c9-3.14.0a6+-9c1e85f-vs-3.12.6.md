# Results vs. 3.12.6

- fork: python
- ref: 9c1e85fd64cf6a85f7c9
- machine: darwin-arm64
- commit hash: 9c1e85f
- commit date: 2025-03-29
- overall geometric mean: 1.039x faster
- HPT reliability: 51.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.08 sec: 1.05x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 271 ms: 1.77x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 271 ms: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 157 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.7 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.3 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 34.6 ms: 1.10x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 47.1 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 970 ms: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.21 ms: 1.09x slower                                                    |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.02 ms: 2.30x faster                                                    |
| mdp                              | 1.09 sec                                                 | 578 ms: 1.89x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 271 ms: 1.77x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 271 ms: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.53x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.52x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 157 ms: 1.41x faster                                                     |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.46 us: 1.16x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.7 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                     |
| float                            | 37.9 ms                                                  | 34.6 ms: 1.10x faster                                                    |
| go                               | 70.0 ms                                                  | 63.9 ms: 1.10x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 47.1 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.6 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 48.1 ns: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 37.7 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.18 sec: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 46.1 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.58 us: 1.00x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 58.0 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.01x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 970 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.3 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| pyflate                          | 216 ms                                                   | 223 ms: 1.03x slower                                                     |
| pycparser                        | 497 ms                                                   | 514 ms: 1.03x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.33 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| shortest_path                    | 219 ms                                                   | 228 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.04x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 45.4 ms: 1.05x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.44 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 441 us: 1.05x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.08 sec: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 51.3 ms: 1.07x slower                                                    |
| nbody                            | 54.2 ms                                                  | 58.3 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.27 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.4 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 903 us: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.21 ms: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 747 ms: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 371 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| fannkuch                         | 176 ms                                                   | 204 ms: 1.16x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.17 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (6): typing_runtime_protocols, sqlite_synth, deltablue, xml_etree_generate, scimark_sor, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250329-3.14.0a6+-9c1e85f/bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 51.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x