# Results vs. 3.12.6

- fork: python
- ref: bd2ed7c7ce58084c682a
- machine: darwin-arm64
- commit hash: bd2ed7c
- commit date: 2025-05-03
- overall geometric mean: 1.092x faster
- HPT reliability: 96.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                    |
| sphinx         | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.2 ms: 2.00x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.4 ms: 1.11x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.00x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 35.5 ms: 1.45x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 55.2 ms: 1.23x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 974 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.6 us: 1.16x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.28 ms: 1.24x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.33 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.79 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 746 us: 2.69x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.56 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.2 ms: 2.00x faster                                                    |
| mdp                              | 1.09 sec                                                 | 573 ms: 1.90x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 449 us: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 35.5 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| deepcopy                         | 161 us                                                   | 126 us: 1.28x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 55.2 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 832 ns: 1.16x faster                                                     |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.9 ns: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.86 us: 1.11x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                    |
| go                               | 70.0 ms                                                  | 63.4 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                     |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 420 ms: 1.03x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.98 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.00x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 974 ms: 1.02x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.7 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 74.9 us: 1.06x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| json                             | 1.93 ms                                                  | 2.06 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 50.1 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 357 ms: 1.09x slower                                                     |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.4 ms: 1.11x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.77 ms: 1.11x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.7 ms: 1.12x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.4 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.6 us: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.33 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.79 ms: 1.19x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.28 ms: 1.24x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.32 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 585 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.8 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.42x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250503-3.14.0a7+-bd2ed7c-NOGIL/bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 96.38% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x