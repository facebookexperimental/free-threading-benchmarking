# Results vs. 3.12.6

- fork: python
- ref: dc28c3a358221b1e0ae5
- machine: darwin-arm64
- commit hash: dc28c3a
- commit date: 2026-10-23
- overall geometric mean: 1.084x faster
- HPT reliability: 97.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.09x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| sphinx         | 434 ms                                                   | 438 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 295 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 287 ms: 1.56x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 137 ms: 1.25x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 179 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 295 ms: 1.13x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 108 ms: 3.37x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                       |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                        |
| nbody          | 54.2 ms                                                  | 60.1 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 90.9 ms: 1.10x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.04 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.1 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                       |
| tomli_loads          | 957 ms                                                   | 876 ms: 1.09x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 38.4 ms: 1.01x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 106 us: 1.03x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.79 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.21x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.27 ms: 4.86x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 764 us: 2.63x faster                                                        |
| pylint                           | 128 ms                                                   | 51.9 ms: 2.47x faster                                                       |
| mdp                              | 1.09 sec                                                 | 571 ms: 1.91x faster                                                        |
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 461 us: 1.80x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 295 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 287 ms: 1.56x faster                                                        |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 56.0 us: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.27x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 137 ms: 1.25x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 179 ms: 1.25x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 783 ns: 1.24x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.16 us: 1.21x faster                                                       |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                      |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.71 ms: 1.15x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 295 ms: 1.13x faster                                                        |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 48.7 ms: 1.12x faster                                                       |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 90.9 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 876 ms: 1.09x faster                                                        |
| raytrace                         | 145 ms                                                   | 135 ms: 1.08x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 57.2 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.04 ms: 1.06x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.69 us: 1.04x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.2 ms: 1.03x faster                                                       |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.7 ns: 1.02x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.4 ms: 1.02x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.4 ms: 1.01x faster                                                       |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.97 ms: 1.01x faster                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                      |
| sphinx                           | 434 ms                                                   | 438 ms: 1.01x slower                                                        |
| hexiom                           | 3.04 ms                                                  | 3.09 ms: 1.02x slower                                                       |
| deltablue                        | 1.73 ms                                                  | 1.76 ms: 1.02x slower                                                       |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                        |
| unpickle_pure_python             | 103 us                                                   | 106 us: 1.03x slower                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                       |
| generators                       | 21.9 ms                                                  | 22.8 ms: 1.04x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.05x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 346 ms: 1.05x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.0 ms: 1.05x slower                                                       |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                        |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                        |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 713 ms: 1.07x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| 2to3                             | 114 ms                                                   | 125 ms: 1.09x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 52.8 ms: 1.11x slower                                                       |
| nbody                            | 54.2 ms                                                  | 60.1 ms: 1.11x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 467 us: 1.11x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                        |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 63.1 ms: 1.16x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.79 ms: 1.19x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.12 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 241 ms: 1.20x slower                                                        |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.23x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 264 ms: 1.24x slower                                                        |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.3 ms: 1.29x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 108 ms: 3.37x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                                |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-dc28c3a-NOGIL/bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 97.26% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x