# Results vs. 3.12.6

- fork: python
- ref: 3945eaf2fcd9cbc3f306
- machine: darwin-arm64
- commit hash: 3945eaf
- commit date: 2026-11-03
- overall geometric mean: 1.079x faster
- HPT reliability: 97.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                        |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                       |
| sphinx         | 434 ms                                                   | 442 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 111 ms: 1.86x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 296 ms: 1.62x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 295 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 292 ms: 1.53x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 284 ms: 1.17x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.6 ms: 1.07x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 112 ms: 3.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                        |
| nbody          | 54.2 ms                                                  | 58.2 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.01 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.7 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                       |
| tomli_loads          | 957 ms                                                   | 857 ms: 1.12x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.06x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.5 ms: 1.10x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.20 ms: 4.95x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 760 us: 2.64x faster                                                        |
| pylint                           | 128 ms                                                   | 51.7 ms: 2.48x faster                                                       |
| mdp                              | 1.09 sec                                                 | 574 ms: 1.90x faster                                                        |
| async_generators                 | 206 ms                                                   | 111 ms: 1.86x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 458 us: 1.81x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 293 ms: 1.69x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 296 ms: 1.62x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 295 ms: 1.56x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 292 ms: 1.53x faster                                                        |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.7 us: 1.32x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 182 ms: 1.22x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.17 us: 1.20x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 282 ms: 1.20x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.3 ms: 1.18x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 284 ms: 1.17x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.17x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                       |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 88.8 ms: 1.12x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 857 ms: 1.12x faster                                                        |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 19.4 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.6 ms: 1.07x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.01 ms: 1.06x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                       |
| raytrace                         | 145 ms                                                   | 137 ms: 1.06x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 57.6 ms: 1.06x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.66 us: 1.05x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 49.3 ns: 1.03x faster                                                       |
| pycparser                        | 497 ms                                                   | 482 ms: 1.03x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.7 ms: 1.02x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                       |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 8.05 ms: 1.00x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 40.1 ms: 1.01x slower                                                       |
| deltablue                        | 1.73 ms                                                  | 1.75 ms: 1.02x slower                                                       |
| sphinx                           | 434 ms                                                   | 442 ms: 1.02x slower                                                        |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                        |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 40.8 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.1 ms: 1.05x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 347 ms: 1.06x slower                                                        |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                        |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.06x slower                                                        |
| thrift                           | 322 us                                                   | 343 us: 1.06x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                       |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                       |
| nbody                            | 54.2 ms                                                  | 58.2 ms: 1.07x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 52.1 ms: 1.09x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.5 ms: 1.10x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 470 us: 1.12x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 63.7 ms: 1.17x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.58 ms: 1.17x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 237 ms: 1.18x slower                                                        |
| telco                            | 2.61 ms                                                  | 3.11 ms: 1.19x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                        |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 68.1 ms: 1.33x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.4 ms: 1.54x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 112 ms: 3.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                                |

Benchmark hidden because not significant (4): json, docutils, json_loads, pathlib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261103-3.16.0a1+dev-3945eaf-NOGIL/bm-20261103-macm4pro-arm64-python-3945eaf2fcd9cbc3f306-3.16.0a1+dev-3945eaf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 97.13% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x