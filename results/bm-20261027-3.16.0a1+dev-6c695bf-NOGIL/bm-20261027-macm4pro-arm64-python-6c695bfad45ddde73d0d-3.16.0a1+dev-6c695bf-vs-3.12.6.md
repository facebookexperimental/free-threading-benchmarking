# Results vs. 3.12.6

- fork: python
- ref: 6c695bfad45ddde73d0d
- machine: darwin-arm64
- commit hash: 6c695bf
- commit date: 2026-10-27
- overall geometric mean: 1.077x faster
- HPT reliability: 95.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                       |
| sphinx         | 434 ms                                                   | 441 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 292 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 290 ms: 1.54x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 179 ms: 1.29x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 138 ms: 1.25x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 297 ms: 1.12x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.4 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 49.3 ms: 1.08x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 162 ms: 1.43x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.41x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| pidigits       | 161 ms                                                   | 159 ms: 1.02x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.2 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.01 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.3 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.3 ms: 1.17x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                       |
| tomli_loads          | 957 ms                                                   | 867 ms: 1.10x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.5 ms: 1.01x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.6 ms: 1.11x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 157 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.80 ms: 1.10x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.81 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                       |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.21x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.32 ms: 4.81x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 752 us: 2.67x faster                                                        |
| pylint                           | 128 ms                                                   | 51.0 ms: 2.51x faster                                                       |
| mdp                              | 1.09 sec                                                 | 583 ms: 1.87x faster                                                        |
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 460 us: 1.80x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 292 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 290 ms: 1.54x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                        |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.9 us: 1.32x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.31x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 179 ms: 1.29x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.27x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 138 ms: 1.25x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 180 ms: 1.24x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.09 us: 1.22x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.6 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 58.3 ms: 1.17x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 293 ms: 1.16x faster                                                        |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 297 ms: 1.12x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                       |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 867 ms: 1.10x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.4 ms: 1.09x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                       |
| raytrace                         | 145 ms                                                   | 135 ms: 1.07x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.01 ms: 1.06x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 57.5 ms: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.04x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                       |
| pidigits                         | 161 ms                                                   | 159 ms: 1.02x faster                                                        |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                       |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.5 ms: 1.01x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 8.04 ms: 1.00x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| sphinx                           | 434 ms                                                   | 441 ms: 1.02x slower                                                        |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.77 ms: 1.03x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.1 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                       |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.2 ms: 1.06x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                        |
| thrift                           | 322 us                                                   | 346 us: 1.07x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 49.3 ms: 1.08x slower                                                       |
| nbody                            | 54.2 ms                                                  | 59.2 ms: 1.09x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.80 ms: 1.10x slower                                                       |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 52.9 ms: 1.11x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.6 ms: 1.11x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 467 us: 1.12x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 157 us: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 63.3 ms: 1.16x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.09 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.81 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                        |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 65.8 ms: 1.28x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 162 ms: 1.43x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.8 ms: 1.52x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.41x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (3): logging_silent, async_tree_eager_cpu_io_mixed, json_loads
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261027-3.16.0a1+dev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 95.14% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x