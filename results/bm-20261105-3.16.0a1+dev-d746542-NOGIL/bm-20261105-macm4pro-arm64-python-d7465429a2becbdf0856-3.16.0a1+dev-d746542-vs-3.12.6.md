# Results vs. 3.12.6

- fork: python
- ref: d7465429a2becbdf0856
- machine: darwin-arm64
- commit hash: d746542
- commit date: 2026-11-05
- overall geometric mean: 1.076x faster
- HPT reliability: 95.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| sphinx         | 434 ms                                                   | 442 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x slower                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 113 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 299 ms: 1.66x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 299 ms: 1.61x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 300 ms: 1.53x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 140 ms: 1.27x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 292 ms: 1.14x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.53x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| pidigits       | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.9 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.4 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.6 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                       |
| tomli_loads          | 957 ms                                                   | 878 ms: 1.09x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.3 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.67 ms: 1.17x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                       |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.26 ms: 4.87x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.62x faster                                                        |
| pylint                           | 128 ms                                                   | 51.5 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 581 ms: 1.88x faster                                                        |
| async_generators                 | 206 ms                                                   | 113 ms: 1.82x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 461 us: 1.80x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 299 ms: 1.66x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 299 ms: 1.61x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 300 ms: 1.53x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| deepcopy                         | 161 us                                                   | 110 us: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 54.1 us: 1.31x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 140 ms: 1.27x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.7 ms: 1.27x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.5 us: 1.26x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.21x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                      |
| comprehensions                   | 9.84 us                                                  | 8.28 us: 1.19x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.8 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                       |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 292 ms: 1.14x faster                                                        |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 89.4 ms: 1.11x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 49.0 ms: 1.11x faster                                                       |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                        |
| pidigits                         | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 878 ms: 1.09x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| raytrace                         | 145 ms                                                   | 136 ms: 1.07x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 57.7 ms: 1.06x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.67 us: 1.05x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                        |
| pycparser                        | 497 ms                                                   | 485 ms: 1.02x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 49.8 ns: 1.02x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.6 ms: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.00x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 43.4 ms: 1.00x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                       |
| sphinx                           | 434 ms                                                   | 442 ms: 1.02x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 40.7 ms: 1.02x slower                                                       |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                        |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| deltablue                        | 1.73 ms                                                  | 1.78 ms: 1.03x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.2 ms: 1.06x slower                                                       |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 347 ms: 1.06x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 41.5 ms: 1.07x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.07x slower                                                       |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.3 ms: 1.09x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 728 ms: 1.10x slower                                                        |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 52.6 ms: 1.10x slower                                                       |
| nbody                            | 54.2 ms                                                  | 59.9 ms: 1.10x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 470 us: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                        |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 63.6 ms: 1.16x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.67 ms: 1.17x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 237 ms: 1.18x slower                                                        |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 268 ms: 1.26x slower                                                        |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.1 ms: 1.29x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.3 ms: 1.54x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.53x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (2): json, docutils
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261105-3.16.0a1+dev-d746542-NOGIL/bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 95.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x