# Results vs. 3.12.6

- fork: python
- ref: 94250a7c0f6cbf51ff6b
- machine: darwin-arm64
- commit hash: 94250a7
- commit date: 2026-11-19
- overall geometric mean: 1.194x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| docutils       | 1.02 sec                                                 | 909 ms: 1.12x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.7 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.64 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.5 ms: 1.28x faster                                                       |
| pidigits       | 161 ms                                                   | 149 ms: 1.08x faster                                                        |
| Geometric mean | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 92.2 ms: 1.08x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.1 ms: 1.22x faster                                                       |
| tomli_loads          | 957 ms                                                   | 804 ms: 1.19x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.62 ms: 1.18x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 95.7 us: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.31 ms: 1.04x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.47 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.26x faster                                                       |
| pylint                           | 128 ms                                                   | 52.0 ms: 2.46x faster                                                       |
| mdp                              | 1.09 sec                                                 | 501 ms: 2.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.7 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.3 us: 1.69x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.3 us: 1.57x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.78 us: 1.45x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.64 ms: 1.41x faster                                                       |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| go                               | 70.0 ms                                                  | 52.0 ms: 1.35x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.4 ms: 1.31x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 636 us: 1.31x faster                                                        |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 110 ms: 1.29x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                       |
| nbody                            | 54.2 ms                                                  | 42.5 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.5 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.0 ms: 1.24x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.1 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                      |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 804 ms: 1.19x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 42.8 ns: 1.19x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.62 ms: 1.18x faster                                                       |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.15x faster                                                       |
| k_core                           | 1.12 sec                                                 | 981 ms: 1.14x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| docutils                         | 1.02 sec                                                 | 909 ms: 1.12x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.79 ms: 1.12x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                       |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                        |
| fannkuch                         | 176 ms                                                   | 159 ms: 1.10x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 23.1 ms: 1.10x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.41 ms: 1.08x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 92.2 ms: 1.08x faster                                                       |
| pidigits                         | 161 ms                                                   | 149 ms: 1.08x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 95.7 us: 1.08x faster                                                       |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.05x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| sympy_str                        | 104 ms                                                   | 99.2 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                        |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 637 ms: 1.04x faster                                                        |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 931 ns: 1.04x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                       |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                        |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.31 ms: 1.04x slower                                                       |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.2 ms: 1.06x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.47 ms: 1.13x slower                                                       |
| many_optionals                   | 195 us                                                   | 228 us: 1.17x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.194x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.15x