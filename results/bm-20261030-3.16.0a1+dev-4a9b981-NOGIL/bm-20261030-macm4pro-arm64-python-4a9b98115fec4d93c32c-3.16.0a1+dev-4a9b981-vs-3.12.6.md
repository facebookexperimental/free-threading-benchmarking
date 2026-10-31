# Results vs. 3.12.6

- fork: python
- ref: 4a9b98115fec4d93c32c
- machine: darwin-arm64
- commit hash: 4a9b981
- commit date: 2026-10-30
- overall geometric mean: 1.092x faster
- HPT reliability: 99.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                      |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.01x slower                                                                |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 109 ms: 1.89x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 284 ms: 1.75x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 286 ms: 1.68x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 291 ms: 1.58x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 283 ms: 1.58x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.27x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 178 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 291 ms: 1.15x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.06x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 109 ms: 3.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.2 ms: 1.18x faster                                                       |
| pidigits       | 161 ms                                                   | 157 ms: 1.02x faster                                                        |
| nbody          | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.7 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.98 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 62.7 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                       |
| tomli_loads          | 957 ms                                                   | 876 ms: 1.09x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.85 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.66 ms: 1.19x slower                                                       |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.21x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.19 ms: 4.96x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 761 us: 2.64x faster                                                        |
| pylint                           | 128 ms                                                   | 51.4 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 567 ms: 1.93x faster                                                        |
| async_generators                 | 206 ms                                                   | 109 ms: 1.89x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 461 us: 1.80x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 284 ms: 1.75x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 286 ms: 1.68x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 291 ms: 1.58x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 283 ms: 1.58x faster                                                        |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 13.5 us: 1.36x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 53.2 us: 1.33x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 134 ms: 1.33x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.30 ms: 1.28x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 136 ms: 1.27x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 178 ms: 1.25x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 8.03 us: 1.23x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.19x faster                                                        |
| go                               | 70.0 ms                                                  | 59.1 ms: 1.18x faster                                                       |
| float                            | 37.9 ms                                                  | 32.2 ms: 1.18x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.17x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| json_dumps                       | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 291 ms: 1.15x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.0 ms: 1.13x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 88.7 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.4 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 876 ms: 1.09x faster                                                        |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                        |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 123 ms: 1.07x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 56.8 ms: 1.07x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 8.98 ms: 1.07x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.06x faster                                                        |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.3 ns: 1.03x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.1 ms: 1.03x faster                                                       |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                       |
| pidigits                         | 161 ms                                                   | 157 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 38.3 ms: 1.02x faster                                                       |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                      |
| sympy_integrate                  | 8.02 ms                                                  | 7.93 ms: 1.01x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.74 ms: 1.01x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.01x slower                                                       |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                        |
| generators                       | 21.9 ms                                                  | 22.6 ms: 1.03x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 40.4 ms: 1.04x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 59.9 ms: 1.04x slower                                                       |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 346 ms: 1.05x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.1 ms: 1.06x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.7 ms: 1.06x slower                                                       |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                       |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 718 ms: 1.08x slower                                                        |
| nbody                            | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.1 ms: 1.09x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 53.0 ms: 1.11x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 467 us: 1.11x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 246 ms: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 62.7 ms: 1.15x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.66 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 239 ms: 1.19x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.85 ms: 1.20x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                       |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 64.2 ms: 1.25x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 109 ms: 3.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (2): json_loads, sphinx
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261030-3.16.0a1+dev-4a9b981-NOGIL/bm-20261030-macm4pro-arm64-python-4a9b98115fec4d93c32c-3.16.0a1+dev-4a9b981.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 99.20% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x