# Results vs. 3.12.6

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: darwin-arm64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.136x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 314 ms: 1.58x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 320 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 335 ms: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 175 ms: 1.32x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 338 ms: 1.32x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 179 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                   |
| nbody          | 54.2 ms                                                  | 41.8 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.3 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.9 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.1 us: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 68.5 ms: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.00x faster                                                   |
| pylint                           | 128 ms                                                   | 56.8 ms: 2.26x faster                                                   |
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.0 us: 1.66x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 314 ms: 1.58x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 123 ms: 1.45x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.81 us: 1.44x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 320 ms: 1.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 335 ms: 1.43x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.6 us: 1.43x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 175 ms: 1.32x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 338 ms: 1.32x faster                                                    |
| go                               | 70.0 ms                                                  | 53.2 ms: 1.32x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.30x faster                                                   |
| nbody                            | 54.2 ms                                                  | 41.8 ms: 1.30x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 179 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.7 ms: 1.22x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                   |
| pyflate                          | 216 ms                                                   | 184 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.0 ms: 1.17x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.0 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                   |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.5 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.7 ms: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.3 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| docutils                         | 1.02 sec                                                 | 954 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.92 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 927 ns: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.7 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.1 us: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 643 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.7 ms: 1.01x faster                                                   |
| thrift                           | 322 us                                                   | 319 us: 1.01x faster                                                    |
| pycparser                        | 497 ms                                                   | 493 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.9 ms: 1.01x slower                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 68.5 ms: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 424 us: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                   |
| many_optionals                   | 195 us                                                   | 243 us: 1.25x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 105 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): create_gc_cycles
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.136x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x