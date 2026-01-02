# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.238x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                            |
| html5lib       | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                           |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                            |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                            |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                            |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                            |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                           |
| async_tree_none_tg               | 172 ms                                                   | 98.6 ms: 1.75x faster                                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                            |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                            |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                            |
| async_tree_eager                 | 45.6 ms                                                  | 38.1 ms: 1.20x faster                                                           |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                            |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                           |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                           |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                           |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                    | 1.30x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.1 ms: 1.36x faster                                                           |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                           |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                           |
| regex_v8       | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 73.1 us: 1.41x faster                                                           |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                           |
| xml_etree_generate   | 38.9 ms                                                  | 30.7 ms: 1.27x faster                                                           |
| pickle_pure_python   | 139 us                                                   | 113 us: 1.23x faster                                                            |
| xml_etree_process    | 26.7 ms                                                  | 21.9 ms: 1.22x faster                                                           |
| tomli_loads          | 957 ms                                                   | 809 ms: 1.18x faster                                                            |
| json_dumps           | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                           |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                           |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                           |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                           |
| python_startup_no_site | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                           |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|-----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.91 ms: 1.22x faster                                                           |
| genshi_text     | 10.5 ms                                                  | 8.89 ms: 1.18x faster                                                           |
| genshi_xml      | 21.8 ms                                                  | 20.5 ms: 1.06x faster                                                           |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                    | 1.11x faster                                                                    |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.92 ms: 5.29x faster                                                           |
| richards                         | 22.4 ms                                                  | 9.77 ms: 2.29x faster                                                           |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                            |
| richards_super                   | 25.4 ms                                                  | 11.6 ms: 2.18x faster                                                           |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                            |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                            |
| mdp                              | 1.09 sec                                                 | 585 ms: 1.86x faster                                                            |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                           |
| async_tree_none_tg               | 172 ms                                                   | 98.6 ms: 1.75x faster                                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                            |
| deepcopy                         | 161 us                                                   | 97.8 us: 1.65x faster                                                           |
| float                            | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                           |
| go                               | 70.0 ms                                                  | 43.2 ms: 1.62x faster                                                           |
| async_tree_memoization           | 223 ms                                                   | 138 ms: 1.61x faster                                                            |
| comprehensions                   | 9.84 us                                                  | 6.16 us: 1.60x faster                                                           |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                           |
| deltablue                        | 1.73 ms                                                  | 1.12 ms: 1.54x faster                                                           |
| logging_silent                   | 50.9 ns                                                  | 33.7 ns: 1.51x faster                                                           |
| pyflate                          | 216 ms                                                   | 145 ms: 1.49x faster                                                            |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.45x faster                                                           |
| scimark_sor                      | 61.0 ms                                                  | 42.1 ms: 1.45x faster                                                           |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.5 ms: 1.43x faster                                                           |
| unpickle_pure_python             | 103 us                                                   | 73.1 us: 1.41x faster                                                           |
| scimark_lu                       | 51.3 ms                                                  | 36.5 ms: 1.41x faster                                                           |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                            |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                           |
| regex_compile                    | 54.6 ms                                                  | 40.1 ms: 1.36x faster                                                           |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                           |
| raytrace                         | 145 ms                                                   | 107 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.34x faster                                                            |
| spectral_norm                    | 54.4 ms                                                  | 40.8 ms: 1.33x faster                                                           |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 255 ms: 1.33x faster                                                            |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                           |
| chaos                            | 28.9 ms                                                  | 22.0 ms: 1.32x faster                                                           |
| k_core                           | 1.12 sec                                                 | 867 ms: 1.29x faster                                                            |
| pprint_pformat                   | 665 ms                                                   | 524 ms: 1.27x faster                                                            |
| pprint_safe_repr                 | 328 ms                                                   | 259 ms: 1.27x faster                                                            |
| xml_etree_generate               | 38.9 ms                                                  | 30.7 ms: 1.27x faster                                                           |
| crypto_pyaes                     | 38.8 ms                                                  | 31.1 ms: 1.25x faster                                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                            |
| pickle_pure_python               | 139 us                                                   | 113 us: 1.23x faster                                                            |
| mako                             | 4.77 ms                                                  | 3.91 ms: 1.22x faster                                                           |
| xml_etree_process                | 26.7 ms                                                  | 21.9 ms: 1.22x faster                                                           |
| logging_simple                   | 2.57 us                                                  | 2.11 us: 1.22x faster                                                           |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.85 sec: 1.21x faster                                                          |
| logging_format                   | 2.80 us                                                  | 2.32 us: 1.21x faster                                                           |
| async_tree_eager                 | 45.6 ms                                                  | 38.1 ms: 1.20x faster                                                           |
| tomli_loads                      | 957 ms                                                   | 809 ms: 1.18x faster                                                            |
| genshi_text                      | 10.5 ms                                                  | 8.89 ms: 1.18x faster                                                           |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                           |
| json_dumps                       | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                           |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                           |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.15x faster                                                            |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                           |
| typing_runtime_protocols         | 71.0 us                                                  | 62.3 us: 1.14x faster                                                           |
| html5lib                         | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                           |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                           |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                           |
| pycparser                        | 497 ms                                                   | 440 ms: 1.13x faster                                                            |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                           |
| thrift                           | 322 us                                                   | 289 us: 1.11x faster                                                            |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                            |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                           |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                            |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                           |
| genshi_xml                       | 21.8 ms                                                  | 20.5 ms: 1.06x faster                                                           |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                            |
| meteor_contest                   | 47.7 ms                                                  | 45.6 ms: 1.05x faster                                                           |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                           |
| telco                            | 2.61 ms                                                  | 2.52 ms: 1.04x faster                                                           |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                           |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                            |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                           |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                            |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                            |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                           |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                            |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                            |
| regex_v8                         | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                           |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                            |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.02x slower                                                            |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                           |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                           |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                            |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                           |
| python_startup_no_site           | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                           |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                            |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                            |
| coverage                         | 26.9 ms                                                  | 33.8 ms: 1.26x slower                                                           |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                           |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                    |

Benchmark hidden because not significant (3): pylint, sqlite_synth, docutils
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-b1e4adf-JIT/bm-20260101-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.238x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.25x