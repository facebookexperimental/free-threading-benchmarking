# Results vs. 3.12.6

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: darwin-arm64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.089x faster
- HPT reliability: 94.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 24.8 ms: 1.08x slower                                                   |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.0 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.8 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| pidigits       | 161 ms                                                   | 172 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 997 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.92 ms: 1.24x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 794 us: 2.53x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.82 ms: 2.11x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.0 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 576 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 488 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| deepcopy                         | 161 us                                                   | 121 us: 1.33x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.92 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 833 ns: 1.16x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.6 ms: 1.16x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.9 ns: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.09x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.60 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 476 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.9 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.28 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.03 ms: 1.00x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 997 ms: 1.04x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.92 us: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                   |
| pidigits                         | 161 ms                                                   | 172 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.8 ms: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| shortest_path                    | 219 ms                                                   | 237 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 719 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.8 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.5 ms: 1.09x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.8 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.9 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 225 ms: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.9 ms: 1.15x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.22 ms: 1.23x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.92 ms: 1.24x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                   |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 580 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, xml_etree_process
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 94.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x