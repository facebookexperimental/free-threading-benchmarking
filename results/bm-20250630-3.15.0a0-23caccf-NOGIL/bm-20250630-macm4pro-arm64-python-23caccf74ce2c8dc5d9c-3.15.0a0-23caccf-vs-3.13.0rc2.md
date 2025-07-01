# Results vs. 3.13.0rc2

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: darwin-arm64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.010x faster
- HPT reliability: 88.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                  |
| html5lib       | 23.1 ms                                                        | 24.8 ms: 1.07x slower                                                   |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.8 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 172 ms: 1.04x slower                                                    |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.92 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.17 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 794 us: 2.57x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 207 ms: 2.54x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 488 us: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 200 ms: 2.03x faster                                                    |
| mdp                              | 1.06 sec                                                       | 576 ms: 1.84x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 212 ms: 1.82x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.0 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 238 ms: 1.26x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 121 us: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.19x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 833 ns: 1.14x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| fannkuch                         | 179 ms                                                         | 179 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 172 ms: 1.04x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.22 ms: 1.05x slower                                                   |
| shortest_path                    | 225 ms                                                         | 237 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.03 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.07 ms: 1.07x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.8 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| connected_components             | 208 ms                                                         | 225 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 352 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.60 ms: 1.10x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 719 ms: 1.11x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.9 ns: 1.11x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.5 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.9 ms: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.9 us: 1.13x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.9 ms: 1.13x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.92 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.8 ms: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.92 us: 1.16x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.4 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.92 us: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.17 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.27x slower                                                   |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.72 ms: 1.30x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 55.8 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 580 us: 1.41x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.82 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): tomli_loads, json_dumps, coroutines
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250630-3.15.0a0-23caccf-NOGIL/bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 88.62% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x