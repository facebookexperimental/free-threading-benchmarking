# Results vs. 3.12.6

- fork: python
- ref: b70d45ab22e1d0f3b8a0
- machine: darwin-arm64
- commit hash: b70d45a
- commit date: 2025-03-21
- overall geometric mean: 1.020x slower
- HPT reliability: 99.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                    |
| sphinx         | 434 ms                                                   | 439 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 192 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 56.6 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 36.3 ms: 1.04x faster                                                    |
| nbody          | 54.2 ms                                                  | 78.7 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.00x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 9.64 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 41.3 ms: 1.06x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.08 sec: 1.12x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.7 ms: 1.15x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 170 us: 1.22x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.26 ms: 1.24x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.22 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| mako            | 4.77 ms                                                  | 6.25 ms: 1.31x slower                                                    |
| django_template | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.41 ms: 2.21x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 925 us: 2.17x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 502 us: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| deepcopy                         | 161 us                                                   | 129 us: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 845 ns: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                    |
| async_generators                 | 206 ms                                                   | 192 ms: 1.07x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.06x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 17.3 us: 1.06x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.39 us: 1.05x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                    |
| float                            | 37.9 ms                                                  | 36.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.00x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.64 ms: 1.01x slower                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.25 sec: 1.01x slower                                                   |
| sphinx                           | 434 ms                                                   | 439 ms: 1.01x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.2 ms: 1.01x slower                                                    |
| generators                       | 21.9 ms                                                  | 22.3 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 508 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| comprehensions                   | 9.84 us                                                  | 10.1 us: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 41.3 ms: 1.06x slower                                                    |
| go                               | 70.0 ms                                                  | 74.8 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 348 us: 1.08x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.19 sec: 1.09x slower                                                   |
| spectral_norm                    | 54.4 ms                                                  | 59.2 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                     |
| regex_compile                    | 54.6 ms                                                  | 59.5 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.3 ms: 1.10x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 56.2 ns: 1.10x slower                                                    |
| pyflate                          | 216 ms                                                   | 239 ms: 1.11x slower                                                     |
| raytrace                         | 145 ms                                                   | 161 ms: 1.11x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 63.8 ms: 1.11x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.86 us: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.08 sec: 1.12x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 9.05 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.90 ms: 1.14x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 69.7 ms: 1.14x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 49.7 ms: 1.14x slower                                                    |
| sympy_str                        | 104 ms                                                   | 119 ms: 1.15x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 30.7 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.22 ms: 1.15x slower                                                    |
| chaos                            | 28.9 ms                                                  | 33.3 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 81.7 us: 1.15x slower                                                    |
| 2to3                             | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 164 ms: 1.16x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 2.00 ms: 1.16x slower                                                    |
| connected_components             | 201 ms                                                   | 235 ms: 1.17x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 46.3 ms: 1.19x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 203 ms: 1.21x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.52 ms: 1.22x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 170 us: 1.22x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.26 ms: 1.24x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 31.4 ms: 1.24x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 56.6 ms: 1.24x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.25x slower                                                     |
| richards                         | 22.4 ms                                                  | 28.0 ms: 1.25x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.4 ms: 1.26x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 415 ms: 1.26x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 60.5 ms: 1.27x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 844 ms: 1.27x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| fannkuch                         | 176 ms                                                   | 227 ms: 1.30x slower                                                     |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| mako                             | 4.77 ms                                                  | 6.25 ms: 1.31x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 67.3 ms: 1.31x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.99 ms: 1.31x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.62 ms: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                    |
| nbody                            | 54.2 ms                                                  | 78.7 ms: 1.45x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 625 us: 1.49x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.3 ms: 2.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (2): pylint, pidigits
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-b70d45a-NOGIL/bm-20250321-macm4pro-arm64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.73% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x