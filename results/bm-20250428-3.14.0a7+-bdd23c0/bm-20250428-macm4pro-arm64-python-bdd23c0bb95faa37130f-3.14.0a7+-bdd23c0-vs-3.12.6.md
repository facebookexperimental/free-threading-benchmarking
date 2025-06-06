# Results vs. 3.12.6

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: darwin-arm64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 258 ms: 1.21x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.6 us: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 918 ms: 1.04x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.95 ms: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.04 ms: 1.06x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.88 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| mako            | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.75 ms: 2.37x faster                                                    |
| mdp                              | 1.09 sec                                                 | 510 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 249 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                    |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.63 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 271 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                     |
| go                               | 70.0 ms                                                  | 57.0 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.7 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.2 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 940 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.7 ms: 1.15x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.15x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.29 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                     |
| sympy_str                        | 104 ms                                                   | 97.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.88 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.8 ms: 1.05x faster                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 44.4 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.6 us: 1.04x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 918 ms: 1.04x faster                                                     |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| pycparser                        | 497 ms                                                   | 483 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                     |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 163 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                     |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 673 ms: 1.01x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.3 ms: 1.01x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.25 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 440 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.04 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 888 us: 1.07x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.97 ms: 1.14x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.95 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                     |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 258 ms: 1.21x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x