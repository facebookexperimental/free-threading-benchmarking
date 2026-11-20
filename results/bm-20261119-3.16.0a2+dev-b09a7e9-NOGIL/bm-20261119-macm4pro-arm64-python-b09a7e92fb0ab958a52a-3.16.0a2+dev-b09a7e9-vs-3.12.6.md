# Results vs. 3.12.6

- fork: python
- ref: b09a7e92fb0ab958a52a
- machine: darwin-arm64
- commit hash: b09a7e9
- commit date: 2026-11-19
- overall geometric mean: 1.062x faster
- HPT reliability: 86.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 128 ms: 1.12x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| sphinx         | 434 ms                                                   | 452 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                    | 1.04x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 111 ms: 1.85x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 302 ms: 1.64x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 302 ms: 1.59x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 298 ms: 1.49x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 183 ms: 1.26x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 144 ms: 1.24x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 142 ms: 1.21x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 299 ms: 1.12x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 272 ms: 1.28x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.46x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.58x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pidigits       | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| nbody          | 54.2 ms                                                  | 60.8 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.0 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                       |
| tomli_loads          | 957 ms                                                   | 861 ms: 1.11x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.3 ms: 1.10x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 158 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.02 ms: 1.13x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.20x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.33 ms: 4.80x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 808 us: 2.49x faster                                                        |
| pylint                           | 128 ms                                                   | 52.8 ms: 2.42x faster                                                       |
| mdp                              | 1.09 sec                                                 | 578 ms: 1.89x faster                                                        |
| async_generators                 | 206 ms                                                   | 111 ms: 1.85x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 478 us: 1.74x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 302 ms: 1.64x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 302 ms: 1.59x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 298 ms: 1.49x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                        |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 54.2 us: 1.31x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 183 ms: 1.26x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 144 ms: 1.24x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 142 ms: 1.21x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.26 us: 1.19x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                      |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 60.0 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| float                            | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.79 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 299 ms: 1.12x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 60.9 ms: 1.12x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 861 ms: 1.11x faster                                                        |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                      |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                       |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                       |
| pidigits                         | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| raytrace                         | 145 ms                                                   | 137 ms: 1.06x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 58.6 ms: 1.04x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.0 ns: 1.04x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.75 us: 1.02x faster                                                       |
| pycparser                        | 497 ms                                                   | 493 ms: 1.01x faster                                                        |
| chaos                            | 28.9 ms                                                  | 28.8 ms: 1.00x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 233 ms: 1.01x slower                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                       |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                       |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.79 ms: 1.04x slower                                                       |
| sphinx                           | 434 ms                                                   | 452 ms: 1.04x slower                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                       |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                        |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.07x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 61.4 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                        |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.7 ms: 1.08x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.3 ms: 1.10x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.0 ms: 1.10x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 736 ms: 1.11x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 469 us: 1.12x slower                                                        |
| 2to3                             | 114 ms                                                   | 128 ms: 1.12x slower                                                        |
| nbody                            | 54.2 ms                                                  | 60.8 ms: 1.12x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 9.02 ms: 1.13x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 158 us: 1.14x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                       |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 64.0 ms: 1.17x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 272 ms: 1.28x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 66.7 ms: 1.30x slower                                                       |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.46x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.3 ms: 1.54x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.58x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                                |

Benchmark hidden because not significant (2): nqueens, html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-b09a7e9-NOGIL/bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 86.81% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x