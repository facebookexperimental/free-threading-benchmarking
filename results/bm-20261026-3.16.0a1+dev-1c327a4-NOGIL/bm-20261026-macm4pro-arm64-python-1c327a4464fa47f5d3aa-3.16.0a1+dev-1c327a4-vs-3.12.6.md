# Results vs. 3.12.6

- fork: python
- ref: 1c327a4464fa47f5d3aa
- machine: darwin-arm64
- commit hash: 1c327a4
- commit date: 2026-10-26
- overall geometric mean: 1.092x faster
- HPT reliability: 99.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                      |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| sphinx         | 434 ms                                                   | 437 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                    | 1.01x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 109 ms: 1.90x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 285 ms: 1.74x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 286 ms: 1.68x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 291 ms: 1.58x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 283 ms: 1.58x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 175 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 135 ms: 1.28x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 285 ms: 1.19x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 290 ms: 1.15x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 179 ms: 1.06x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 107 ms: 3.34x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                       |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                        |
| nbody          | 54.2 ms                                                  | 59.0 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.6 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 62.8 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                       |
| tomli_loads          | 957 ms                                                   | 884 ms: 1.08x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.04x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                       |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.19 ms: 4.96x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 747 us: 2.69x faster                                                        |
| pylint                           | 128 ms                                                   | 50.5 ms: 2.54x faster                                                       |
| mdp                              | 1.09 sec                                                 | 572 ms: 1.91x faster                                                        |
| async_generators                 | 206 ms                                                   | 109 ms: 1.90x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 457 us: 1.82x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 285 ms: 1.74x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 286 ms: 1.68x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 291 ms: 1.58x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 283 ms: 1.58x faster                                                        |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.5 us: 1.33x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.32x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 175 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 135 ms: 1.28x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.06 us: 1.22x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 285 ms: 1.19x faster                                                        |
| go                               | 70.0 ms                                                  | 59.0 ms: 1.19x faster                                                       |
| float                            | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 290 ms: 1.15x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.6 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 995 ms: 1.12x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 48.8 ms: 1.11x faster                                                       |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 884 ms: 1.08x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                        |
| raytrace                         | 145 ms                                                   | 135 ms: 1.08x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 57.1 ms: 1.07x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 47.9 ns: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 179 ms: 1.06x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                       |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                       |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.91 ms: 1.01x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                      |
| sphinx                           | 434 ms                                                   | 437 ms: 1.01x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.74 ms: 1.01x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                       |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                        |
| generators                       | 21.9 ms                                                  | 22.6 ms: 1.03x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 59.7 ms: 1.04x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.04x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 40.6 ms: 1.05x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 344 ms: 1.05x slower                                                        |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.7 ms: 1.06x slower                                                       |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 708 ms: 1.07x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                       |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 51.5 ms: 1.08x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 454 us: 1.08x slower                                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| nbody                            | 54.2 ms                                                  | 59.0 ms: 1.09x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 62.8 ms: 1.15x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.80 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                        |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.22x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.3 ms: 1.29x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 107 ms: 3.34x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261026-3.16.0a1+dev-1c327a4-NOGIL/bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 99.18% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x