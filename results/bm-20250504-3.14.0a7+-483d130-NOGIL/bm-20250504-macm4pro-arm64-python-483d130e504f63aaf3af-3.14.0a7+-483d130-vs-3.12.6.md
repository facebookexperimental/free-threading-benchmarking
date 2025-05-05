# Results vs. 3.12.6

- fork: python
- ref: 483d130e504f63aaf3af
- machine: darwin-arm64
- commit hash: 483d130
- commit date: 2025-05-04
- overall geometric mean: 1.097x faster
- HPT reliability: 98.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.3 ms: 1.42x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 973 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.1 us: 1.12x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.29 ms: 1.24x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.31 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.78 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 738 us: 2.72x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.44x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.51 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 1.99x faster                                                    |
| mdp                              | 1.09 sec                                                 | 570 ms: 1.92x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 450 us: 1.84x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.3 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| deepcopy                         | 161 us                                                   | 124 us: 1.31x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.30x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| pylint                           | 128 ms                                                   | 111 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.70 us: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.0 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.13x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.31 us: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.8 ms: 1.11x faster                                                    |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.2 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.2 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 52.4 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 973 ms: 1.02x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.63 us: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.8 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.9 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.1 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 74.4 us: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.05x slower                                                     |
| json                             | 1.93 ms                                                  | 2.04 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.06x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.5 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.61 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                     |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 727 ms: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.1 us: 1.12x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.6 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.7 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.31 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.78 ms: 1.19x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.29 ms: 1.24x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.29 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 604 us: 1.44x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250504-3.14.0a7+-483d130-NOGIL/bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7+-483d130.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 98.15% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x