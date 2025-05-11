# Results vs. 3.12.6

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.5 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.8 ms: 1.15x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.22 ms: 1.23x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.51 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.09 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.4 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.56 ms: 2.17x faster                                                   |
| mdp                              | 1.09 sec                                                 | 534 ms: 2.05x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.90 us: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| go                               | 70.0 ms                                                  | 56.7 ms: 1.23x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.9 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 47.1 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.8 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.4 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.08x faster                                                   |
| nbody                            | 54.2 ms                                                  | 50.5 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 66.4 us: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.9 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.7 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 656 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.4 ms: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 960 ns: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                   |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.1 ms: 1.01x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 101 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.51 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.09 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 945 us: 1.14x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.22 ms: 1.23x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (4): pycparser, tomli_loads, pprint_safe_repr, richards
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x