# Results vs. 3.12.6

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.082x faster
- HPT reliability: 95.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 25.9 ms: 1.12x slower                                                   |
| sphinx         | 434 ms                                                   | 420 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.02x faster                                                   |
| tomli_loads          | 957 ms                                                   | 986 ms: 1.03x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                    |
| json_loads           | 10.9 us                                                  | 12.6 us: 1.17x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.27 ms: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.39 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.83 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 778 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.68 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 579 ms: 1.89x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 482 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.4 us: 1.27x faster                                                   |
| deepcopy                         | 161 us                                                   | 127 us: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.81 us: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 62.9 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 56.9 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.6 ms: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 420 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.00 ms: 1.00x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 986 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| chaos                            | 28.9 ms                                                  | 30.0 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 76.0 us: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| json                             | 1.93 ms                                                  | 2.09 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 359 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.3 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.85 us: 1.11x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.12x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.9 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.6 ms: 1.16x slower                                                   |
| json_loads                       | 10.9 us                                                  | 12.6 us: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.39 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.83 ms: 1.20x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.27 ms: 1.24x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.38 ms: 1.29x slower                                                   |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 67.0 ms: 1.31x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, scimark_fft
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-NOGIL/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 95.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x