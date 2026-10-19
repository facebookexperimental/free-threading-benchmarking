# Results vs. 3.12.6

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: darwin-arm64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.073x faster
- HPT reliability: 95.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                       |
| sphinx         | 434 ms                                                   | 439 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 290 ms: 1.66x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 294 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 286 ms: 1.56x faster                                                        |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.29x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 138 ms: 1.25x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.26x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.43x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.8 ms: 1.16x faster                                                       |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.3 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 90.7 ms: 1.10x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.4 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                       |
| tomli_loads          | 957 ms                                                   | 880 ms: 1.09x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                        |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.83 ms: 1.23x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                       |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.22x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.21 ms: 4.93x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                        |
| pylint                           | 128 ms                                                   | 52.4 ms: 2.44x faster                                                       |
| mdp                              | 1.09 sec                                                 | 589 ms: 1.85x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 456 us: 1.82x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 290 ms: 1.66x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 294 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 286 ms: 1.56x faster                                                        |
| deepcopy                         | 161 us                                                   | 109 us: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 138 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.29x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.4 us: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 56.7 us: 1.25x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 138 ms: 1.25x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 786 ns: 1.23x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.8 ms: 1.17x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.42 us: 1.17x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                      |
| float                            | 37.9 ms                                                  | 32.8 ms: 1.16x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 293 ms: 1.14x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.11x faster                                                      |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.3 ms: 1.10x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 90.7 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 880 ms: 1.09x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| raytrace                         | 145 ms                                                   | 135 ms: 1.07x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 57.6 ms: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.06x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.66 us: 1.05x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.11 ms: 1.05x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 42.6 ms: 1.02x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                       |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| chaos                            | 28.9 ms                                                  | 28.6 ms: 1.01x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                        |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 8.05 ms: 1.00x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                      |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                        |
| sphinx                           | 434 ms                                                   | 439 ms: 1.01x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.77 ms: 1.03x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.3 ms: 1.05x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.0 ms: 1.05x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 40.8 ms: 1.05x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                        |
| hexiom                           | 3.04 ms                                                  | 3.20 ms: 1.05x slower                                                       |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.07x slower                                                        |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.9 ms: 1.07x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                       |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                        |
| nbody                            | 54.2 ms                                                  | 59.3 ms: 1.09x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 735 ms: 1.11x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 53.1 ms: 1.11x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                       |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 63.4 ms: 1.16x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                       |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                        |
| telco                            | 2.61 ms                                                  | 3.17 ms: 1.21x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 9.83 ms: 1.23x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| scimark_lu                       | 51.3 ms                                                  | 64.1 ms: 1.25x slower                                                       |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.26x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 574 us: 1.37x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.43x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (2): logging_silent, xml_etree_generate
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261018-3.16.0a1+dev-7dbc797-NOGIL/bm-20261018-macm4pro-arm64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 95.45% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.28x