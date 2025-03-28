# Results vs. 3.12.6

- fork: python
- ref: 8a00c9a4d2ce9d373b13
- machine: darwin-arm64
- commit hash: 8a00c9a
- commit date: 2025-03-27
- overall geometric mean: 1.000x faster
- HPT reliability: 97.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 131 ms: 1.15x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| sphinx         | 434 ms                                                   | 440 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.1 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 201 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 55.1 ms: 1.21x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                    |
| nbody          | 54.2 ms                                                  | 73.8 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 58.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 40.9 ms: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.06 sec: 1.11x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.4 ms: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 169 us: 1.21x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 126 us: 1.22x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.21 ms: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.24 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.1 ms: 1.20x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.9 ms: 1.23x slower                                                    |
| mako            | 4.77 ms                                                  | 6.10 ms: 1.28x slower                                                    |
| django_template | 13.6 ms                                                  | 18.2 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.35 ms: 2.22x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 925 us: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 230 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| mdp                              | 1.09 sec                                                 | 636 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 502 us: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                    |
| deepcopy                         | 161 us                                                   | 127 us: 1.27x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.1 ms: 1.23x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 841 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 119 ms: 1.11x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| float                            | 37.9 ms                                                  | 35.2 ms: 1.08x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 17.0 us: 1.08x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.05 sec: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.38 us: 1.06x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.7 ms: 1.06x faster                                                    |
| async_generators                 | 206 ms                                                   | 201 ms: 1.03x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.19 sec: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 39.8 ms: 1.00x slower                                                    |
| pycparser                        | 497 ms                                                   | 503 ms: 1.01x slower                                                     |
| generators                       | 21.9 ms                                                  | 22.2 ms: 1.01x slower                                                    |
| sphinx                           | 434 ms                                                   | 440 ms: 1.01x slower                                                     |
| comprehensions                   | 9.84 us                                                  | 10.0 us: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| go                               | 70.0 ms                                                  | 72.2 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| pyflate                          | 216 ms                                                   | 226 ms: 1.05x slower                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 40.9 ms: 1.05x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 58.7 ms: 1.08x slower                                                    |
| spectral_norm                    | 54.4 ms                                                  | 58.7 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.7 ms: 1.08x slower                                                    |
| raytrace                         | 145 ms                                                   | 157 ms: 1.09x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 233 ms: 1.10x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 47.7 ms: 1.10x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 55.9 ns: 1.10x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.3 ms: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.84 us: 1.11x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.06 sec: 1.11x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.12x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 68.5 ms: 1.12x slower                                                    |
| shortest_path                    | 219 ms                                                   | 246 ms: 1.13x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 79.9 us: 1.13x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 30.4 ms: 1.14x slower                                                    |
| chaos                            | 28.9 ms                                                  | 32.9 ms: 1.14x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.89 ms: 1.14x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.37 ms: 1.14x slower                                                    |
| sympy_str                        | 104 ms                                                   | 119 ms: 1.15x slower                                                     |
| 2to3                             | 114 ms                                                   | 131 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.24 ms: 1.15x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.01 ms: 1.16x slower                                                    |
| connected_components             | 201 ms                                                   | 234 ms: 1.17x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 46.4 ms: 1.19x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 26.1 ms: 1.20x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 55.1 ms: 1.21x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 202 ms: 1.21x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 169 us: 1.21x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 126 us: 1.22x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.21 ms: 1.22x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 31.1 ms: 1.23x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.9 ms: 1.23x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 39.7 ms: 1.23x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 59.1 ms: 1.24x slower                                                    |
| fannkuch                         | 176 ms                                                   | 217 ms: 1.24x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 64.1 ms: 1.25x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 411 ms: 1.25x slower                                                     |
| richards                         | 22.4 ms                                                  | 28.1 ms: 1.26x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 837 ms: 1.26x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.86 ms: 1.27x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.10 ms: 1.28x slower                                                    |
| many_optionals                   | 195 us                                                   | 253 us: 1.29x slower                                                     |
| django_template                  | 13.6 ms                                                  | 18.2 ms: 1.33x slower                                                    |
| nbody                            | 54.2 ms                                                  | 73.8 ms: 1.36x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.56 ms: 1.37x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 590 us: 1.41x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.2 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (3): pylint, pidigits, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250327-3.14.0a6+-8a00c9a-NOGIL/bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 97.16% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x