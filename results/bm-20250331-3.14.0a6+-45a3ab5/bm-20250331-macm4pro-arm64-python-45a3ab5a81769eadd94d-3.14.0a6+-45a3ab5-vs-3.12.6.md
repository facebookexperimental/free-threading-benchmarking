# Results vs. 3.12.6

- fork: python
- ref: 45a3ab5a81769eadd94d
- machine: darwin-arm64
- commit hash: 45a3ab5
- commit date: 2025-03-31
- overall geometric mean: 1.046x faster
- HPT reliability: 72.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.88x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 267 ms: 1.79x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 269 ms: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 152 ms: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.6 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 134 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 34.5 ms: 1.10x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.6 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.98 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 47.4 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| tomli_loads          | 957 ms                                                   | 970 ms: 1.01x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.06x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.08 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| mako            | 4.77 ms                                                  | 5.17 ms: 1.08x slower                                                    |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.96 ms: 2.32x faster                                                    |
| mdp                              | 1.09 sec                                                 | 576 ms: 1.89x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.88x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 267 ms: 1.79x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 269 ms: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 152 ms: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.44x faster                                                     |
| deepcopy                         | 161 us                                                   | 116 us: 1.39x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.6 ms: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.41 us: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                     |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                     |
| go                               | 70.0 ms                                                  | 63.6 ms: 1.10x faster                                                    |
| float                            | 37.9 ms                                                  | 34.5 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 47.4 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 47.6 ns: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.6 ms: 1.07x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 37.5 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.6 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.16 sec: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.9 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 70.5 us: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.79 us: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.8 ms: 1.00x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 61.6 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 970 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                                    |
| pyflate                          | 216 ms                                                   | 220 ms: 1.02x slower                                                     |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.02x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 510 ms: 1.03x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 45.1 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.98 ms: 1.04x slower                                                    |
| shortest_path                    | 219 ms                                                   | 228 ms: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.43 ms: 1.05x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 53.9 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 441 us: 1.05x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.1 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.9 ms: 1.06x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.4 ms: 1.06x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.23 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 178 ms: 1.06x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.3 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.06x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 891 us: 1.07x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.17 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 749 ms: 1.13x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 373 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| fannkuch                         | 176 ms                                                   | 205 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 134 ms: 1.19x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.08 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 239 us: 1.22x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (5): scimark_fft, logging_simple, deltablue, asyncio_websockets, sympy_sum
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250331-3.14.0a6+-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 72.25% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x