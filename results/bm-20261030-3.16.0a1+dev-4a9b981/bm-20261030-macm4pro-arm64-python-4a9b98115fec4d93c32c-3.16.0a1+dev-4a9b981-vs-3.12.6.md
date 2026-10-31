# Results vs. 3.12.6

- fork: python
- ref: 4a9b98115fec4d93c32c
- machine: darwin-arm64
- commit hash: 4a9b981
- commit date: 2026-10-30
- overall geometric mean: 1.207x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| docutils       | 1.02 sec                                                 | 890 ms: 1.15x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.1 ms: 1.15x faster                                                       |
| sphinx         | 434 ms                                                   | 383 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.77 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.4 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.21x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.6 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                       |
| tomli_loads          | 957 ms                                                   | 790 ms: 1.21x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 91.6 us: 1.12x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.12 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.47 ms: 1.07x faster                                                       |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.89 ms: 5.34x faster                                                       |
| pylint                           | 128 ms                                                   | 49.9 ms: 2.57x faster                                                       |
| mdp                              | 1.09 sec                                                 | 494 ms: 2.21x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 263 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 94.2 us: 1.71x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.9 us: 1.55x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.53 us: 1.51x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                        |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.41x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.77 ms: 1.39x faster                                                       |
| go                               | 70.0 ms                                                  | 51.6 ms: 1.36x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 614 us: 1.35x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.5 ms: 1.31x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.9 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.3 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 48.7 ms: 1.25x faster                                                       |
| nbody                            | 54.2 ms                                                  | 43.4 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 115 ms: 1.23x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 790 ms: 1.21x faster                                                        |
| pyflate                          | 216 ms                                                   | 179 ms: 1.21x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.9 ms: 1.20x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.18x faster                                                      |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.79 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 969 ms: 1.15x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.75 ms: 1.15x faster                                                       |
| docutils                         | 1.02 sec                                                 | 890 ms: 1.15x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.1 ms: 1.15x faster                                                       |
| sphinx                           | 434 ms                                                   | 383 ms: 1.13x faster                                                        |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.3 ms: 1.13x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.5 ms: 1.13x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 91.6 us: 1.12x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.6 ms: 1.12x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.18 ms: 1.12x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.0 ms: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.10x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                        |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                        |
| sympy_str                        | 104 ms                                                   | 97.1 ms: 1.07x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.47 ms: 1.07x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 53.9 ms: 1.07x faster                                                       |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.07x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 625 ms: 1.06x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 911 ns: 1.06x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 8.12 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                        |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.4 ms: 1.07x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                       |
| many_optionals                   | 195 us                                                   | 225 us: 1.15x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.6 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261030-3.16.0a1+dev-4a9b981/bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.207x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x