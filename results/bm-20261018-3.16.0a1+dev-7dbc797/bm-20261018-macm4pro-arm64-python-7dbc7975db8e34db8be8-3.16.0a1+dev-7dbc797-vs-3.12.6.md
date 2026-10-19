# Results vs. 3.12.6

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: darwin-arm64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.191x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                        |
| docutils       | 1.02 sec                                                 | 901 ms: 1.13x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.6 ms: 1.12x faster                                                       |
| sphinx         | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 264 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.46x faster                                                        |
| async_generators                 | 206 ms                                                   | 142 ms: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.73 ms: 1.39x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 273 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.3 ms: 1.28x faster                                                       |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.21x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.4 ms: 1.25x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                       |
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 92.9 us: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.39 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.47 ms: 1.07x faster                                                       |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.97 ms: 5.24x faster                                                       |
| pylint                           | 128 ms                                                   | 51.9 ms: 2.47x faster                                                       |
| mdp                              | 1.09 sec                                                 | 501 ms: 2.18x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 264 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.9 us: 1.68x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.57 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 48.5 us: 1.46x faster                                                       |
| async_generators                 | 206 ms                                                   | 142 ms: 1.46x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.73 ms: 1.39x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.38x faster                                                        |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| go                               | 70.0 ms                                                  | 51.5 ms: 1.36x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 627 us: 1.32x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.3 ms: 1.32x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.8 ms: 1.31x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 110 ms: 1.29x faster                                                        |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| nbody                            | 54.2 ms                                                  | 42.3 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.4 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.4 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 273 ms: 1.24x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 49.4 ms: 1.23x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.12 us: 1.21x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.9 ns: 1.21x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.8 ms: 1.20x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                       |
| pyflate                          | 216 ms                                                   | 181 ms: 1.20x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.5 ms: 1.18x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.18x faster                                                      |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                        |
| k_core                           | 1.12 sec                                                 | 971 ms: 1.15x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.76 ms: 1.14x faster                                                       |
| docutils                         | 1.02 sec                                                 | 901 ms: 1.13x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.6 ms: 1.12x faster                                                       |
| sphinx                           | 434 ms                                                   | 387 ms: 1.12x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                        |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 92.9 us: 1.11x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.9 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.9 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.47 ms: 1.07x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                       |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                        |
| sympy_str                        | 104 ms                                                   | 98.0 ms: 1.06x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                       |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                       |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.05x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 923 ns: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                       |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 48.2 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 43.1 ms: 1.08x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.09x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.11x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.39 ms: 1.12x slower                                                       |
| many_optionals                   | 195 us                                                   | 227 us: 1.16x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.3 ms: 2.90x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                                |

Benchmark hidden because not significant (2): sympy_expand, regex_v8
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261018-3.16.0a1+dev-7dbc797/bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.191x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.18x