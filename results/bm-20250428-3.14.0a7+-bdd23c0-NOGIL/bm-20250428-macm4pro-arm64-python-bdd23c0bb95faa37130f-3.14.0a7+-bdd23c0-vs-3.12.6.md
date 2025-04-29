# Results vs. 3.12.6

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: darwin-arm64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.100x faster
- HPT reliability: 98.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.05x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.37x faster                                                    |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.3 ms: 1.00x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 966 ms: 1.01x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.09x slower                                                     |
| json_loads           | 10.9 us                                                  | 12.5 us: 1.15x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| django_template | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 746 us: 2.69x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 195 ms: 2.46x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.45x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.86 ms: 2.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                    |
| mdp                              | 1.09 sec                                                 | 567 ms: 1.93x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 441 us: 1.88x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 232 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.96 ms: 1.36x faster                                                    |
| deepcopy                         | 161 us                                                   | 124 us: 1.30x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.29x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 815 ns: 1.19x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.58 us: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.5 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| go                               | 70.0 ms                                                  | 62.3 ms: 1.12x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.5 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.1 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.8 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                     |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.97 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.00x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.3 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 966 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.84 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.2 us: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.6 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 224 ms: 1.05x slower                                                     |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| json                             | 1.93 ms                                                  | 2.05 ms: 1.06x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 49.9 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.07x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.09x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.8 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 727 ms: 1.09x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.77 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| json_loads                       | 10.9 us                                                  | 12.5 us: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 594 us: 1.42x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 98.08% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x