# Results vs. 3.12.6

- fork: python
- ref: 45a3ab5a81769eadd94d
- machine: darwin-arm64
- commit hash: 45a3ab5
- commit date: 2025-03-31
- overall geometric mean: 1.052x slower
- HPT reliability: 99.73%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 139 ms: 1.22x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.09 sec: 1.06x slower                                                   |
| html5lib       | 23.0 ms                                                  | 26.0 ms: 1.13x slower                                                    |
| sphinx         | 434 ms                                                   | 450 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.91x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.46x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.08x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 13.0 ms: 1.04x faster                                                    |
| async_generators                 | 206 ms                                                   | 203 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.01x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 60.7 ms: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.4 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| float          | 37.9 ms                                                  | 38.1 ms: 1.00x slower                                                    |
| nbody          | 54.2 ms                                                  | 74.8 ms: 1.38x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 64.8 ms: 1.19x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 42.8 ms: 1.10x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.15 sec: 1.20x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 32.4 ms: 1.21x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.26 ms: 1.24x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 181 us: 1.30x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 141 us: 1.37x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.19 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 28.7 ms: 1.32x slower                                                    |
| mako            | 4.77 ms                                                  | 6.30 ms: 1.32x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 14.7 ms: 1.40x slower                                                    |
| django_template | 13.6 ms                                                  | 20.8 ms: 1.53x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.39x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 923 us: 2.18x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.81 ms: 2.12x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 241 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.91x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 258 ms: 1.78x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 500 us: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                     |
| mdp                              | 1.09 sec                                                 | 666 ms: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.46x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 124 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.3 ms: 1.19x faster                                                    |
| deepcopy                         | 161 us                                                   | 143 us: 1.13x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 862 ns: 1.12x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 91.1 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.08x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 20.2 ms: 1.05x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.05x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 13.0 ms: 1.04x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 12.0 ms: 1.03x faster                                                    |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| async_generators                 | 206 ms                                                   | 203 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| float                            | 37.9 ms                                                  | 38.1 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 232 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                    |
| sphinx                           | 434 ms                                                   | 450 ms: 1.04x slower                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.33 sec: 1.04x slower                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 19.1 us: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.09 sec: 1.06x slower                                                   |
| generators                       | 21.9 ms                                                  | 23.5 ms: 1.07x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| pycparser                        | 497 ms                                                   | 539 ms: 1.08x slower                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.59 us: 1.09x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 42.8 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 124 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.10x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 52.4 ms: 1.12x slower                                                    |
| spectral_norm                    | 54.4 ms                                                  | 61.1 ms: 1.12x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 26.0 ms: 1.13x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 9.16 ms: 1.14x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 58.1 ns: 1.14x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| pyflate                          | 216 ms                                                   | 248 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.19 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 252 ms: 1.15x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 66.8 ms: 1.16x slower                                                    |
| go                               | 70.0 ms                                                  | 81.8 ms: 1.17x slower                                                    |
| comprehensions                   | 9.84 us                                                  | 11.5 us: 1.17x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 6.07 ms: 1.17x slower                                                    |
| raytrace                         | 145 ms                                                   | 172 ms: 1.19x slower                                                     |
| regex_compile                    | 54.6 ms                                                  | 64.8 ms: 1.19x slower                                                    |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 73.2 ms: 1.20x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.15 sec: 1.20x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.50 ms: 1.20x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 32.4 ms: 1.21x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 3.13 us: 1.22x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.41 us: 1.22x slower                                                    |
| 2to3                             | 114 ms                                                   | 139 ms: 1.22x slower                                                     |
| sympy_str                        | 104 ms                                                   | 127 ms: 1.22x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 53.6 ms: 1.23x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 87.6 us: 1.23x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.26 ms: 1.24x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 59.4 ms: 1.25x slower                                                    |
| chaos                            | 28.9 ms                                                  | 36.5 ms: 1.26x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 65.1 ms: 1.27x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.25 ms: 1.27x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.22 ms: 1.29x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 215 ms: 1.29x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 181 us: 1.30x slower                                                     |
| richards                         | 22.4 ms                                                  | 29.3 ms: 1.31x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 33.3 ms: 1.31x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 42.3 ms: 1.31x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 28.7 ms: 1.32x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.30 ms: 1.32x slower                                                    |
| fannkuch                         | 176 ms                                                   | 233 ms: 1.33x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 60.7 ms: 1.33x slower                                                    |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 52.1 ms: 1.34x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 141 us: 1.37x slower                                                     |
| nbody                            | 54.2 ms                                                  | 74.8 ms: 1.38x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 4.21 ms: 1.39x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 14.7 ms: 1.40x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.74 ms: 1.43x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 601 us: 1.43x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 484 ms: 1.48x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 982 ms: 1.48x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                    |
| django_template                  | 13.6 ms                                                  | 20.8 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.4 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x slower                                                             |

Benchmark hidden because not significant (2): pylint, bench_mp_pool
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250331-3.14.0a6+-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.052x slower

# HPT report

- Reliability score: 99.73% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.22x