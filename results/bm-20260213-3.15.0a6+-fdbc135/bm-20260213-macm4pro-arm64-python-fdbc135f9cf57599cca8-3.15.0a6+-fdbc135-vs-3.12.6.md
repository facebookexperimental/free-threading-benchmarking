# Results vs. 3.12.6

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: darwin-arm64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.4 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| tomli_loads          | 957 ms                                                   | 844 ms: 1.13x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.57 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.75 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.01 ms: 5.17x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.11x faster                                                     |
| mdp                              | 1.09 sec                                                 | 529 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 96.4 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.4 us: 1.66x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.01 us: 1.40x faster                                                    |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.1 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| go                               | 70.0 ms                                                  | 53.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.26x faster                                                     |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 895 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.19x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.5 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 844 ms: 1.13x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.5 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.57 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 626 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.1 ms: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.75 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.18 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.85 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260213-3.15.0a6+-fdbc135/bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x