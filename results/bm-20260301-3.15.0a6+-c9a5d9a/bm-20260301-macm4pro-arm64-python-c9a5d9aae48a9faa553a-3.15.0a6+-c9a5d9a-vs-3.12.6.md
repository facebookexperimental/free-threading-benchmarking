# Results vs. 3.12.6

- fork: python
- ref: c9a5d9aae48a9faa553a
- machine: darwin-arm64
- commit hash: c9a5d9a
- commit date: 2026-03-01
- overall geometric mean: 1.169x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.3 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.1 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.9 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 830 ms: 1.15x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.57 ms: 1.10x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.99 ms: 5.21x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| mdp                              | 1.09 sec                                                 | 537 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 231 ms: 1.99x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.3 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.1 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.7 us: 1.67x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.90 us: 1.43x faster                                                    |
| float                            | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 51.9 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.28x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.2 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 893 ms: 1.25x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.2 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.19x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.3 ms: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.38 us: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 830 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.2 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.9 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.2 ms: 1.14x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.7 ms: 1.14x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.1 us: 1.11x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.57 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                    |
| fannkuch                         | 176 ms                                                   | 166 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 308 us: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 637 ms: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.6 us: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 908 us: 1.09x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.9 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (2): pidigits, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260301-3.15.0a6+-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.169x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x