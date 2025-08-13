# Results vs. 3.12.6

- fork: python
- ref: 797c2c33e181badc053f
- machine: darwin-arm64
- commit hash: 797c2c3
- commit date: 2025-08-12
- overall geometric mean: 1.073x faster
- HPT reliability: 92.30%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.10x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 990 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 790 us: 2.54x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.4 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.32x faster                                                   |
| deepcopy                         | 161 us                                                   | 123 us: 1.31x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.30x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 826 ns: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.42 us: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.0 ns: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.6 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.10x faster                                                   |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.7 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.98 ms: 1.07x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.00x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.17 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.8 ms: 1.03x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 990 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.2 us: 1.05x slower                                                   |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.05x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 62.1 ms: 1.08x slower                                                   |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| 2to3                             | 114 ms                                                   | 126 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 224 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.4 ms: 1.12x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 58.1 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.5 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 57.7 ms: 1.21x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 587 us: 1.40x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.50x slower                                                   |
| many_optionals                   | 195 us                                                   | 337 us: 1.73x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250812-3.15.0a0-797c2c3-NOGIL/bm-20250812-macm4pro-arm64-python-797c2c33e181badc053f-3.15.0a0-797c2c3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 92.30% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x