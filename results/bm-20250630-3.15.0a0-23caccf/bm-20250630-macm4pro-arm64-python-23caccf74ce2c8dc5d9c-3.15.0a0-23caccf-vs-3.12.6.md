# Results vs. 3.12.6

- fork: python
- ref: 23caccf74ce2c8dc5d9c
- machine: darwin-arm64
- commit hash: 23caccf
- commit date: 2025-06-30
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 415 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 195 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.8 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 174 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.9 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 910 ms: 1.05x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.00 ms: 1.12x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                  |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 514 ms: 2.12x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.87 ms: 2.10x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 257 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 258 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.53x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.51 us: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 269 ms: 1.26x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.9 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 272 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 963 ms: 1.16x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.5 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.9 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| nbody                            | 54.2 ms                                                  | 47.8 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.8 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.6 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.4 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.07x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 910 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                  |
| sphinx                           | 434 ms                                                   | 415 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.8 ms: 1.04x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.3 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.9 ms: 1.02x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.8 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.9 ms: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 957 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 667 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                    |
| pycparser                        | 497 ms                                                   | 503 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 195 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| json_dumps                       | 4.26 ms                                                  | 4.47 ms: 1.05x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.16 ms: 1.07x slower                                                   |
| pidigits                         | 161 ms                                                   | 174 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.00 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 990 us: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): regex_dna, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250630-3.15.0a0-23caccf/bm-20250630-macm4pro-arm64-python-23caccf74ce2c8dc5d9c-3.15.0a0-23caccf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x