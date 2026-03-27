# Results vs. 3.12.6

- fork: python
- ref: c75d220e257ef7fda8d5
- machine: darwin-arm64
- commit hash: c75d220
- commit date: 2026-03-26
- overall geometric mean: 1.166x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 230 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 1.99x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.6 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.7 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.21x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 812 ms: 1.18x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.17x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 230 ms: 2.08x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 230 ms: 1.99x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.6 ms: 1.78x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.68x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.4 us: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                    |
| float                            | 37.9 ms                                                  | 26.5 ms: 1.43x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.14 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 52.8 ms: 1.33x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.7 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| nbody                            | 54.2 ms                                                  | 44.1 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.5 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 812 ms: 1.18x faster                                                     |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                     |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.5 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.7 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.81 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.2 us: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.42 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 936 ns: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                     |
| thrift                           | 322 us                                                   | 312 us: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.7 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.69 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 901 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.92 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.7 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260326-3.15.0a7+-c75d220/bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.166x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.24x