# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: darwin-arm64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.008x faster
- HPT reliability: 66.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 26.6 ms: 1.15x slower                                                   |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.49x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.57 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 103 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 964 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.6 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.23 ms: 1.12x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 536 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 965 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 57.4 ms: 1.26x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.7 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 964 ms: 1.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 960 us: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.57 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.6 ms: 1.01x faster                                                   |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.6 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.7 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                   |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.08 ms: 1.00x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.4 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.64 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.9 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 665 ms: 1.02x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.3 ms: 1.02x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 67.0 us: 1.04x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.12 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.19 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.1 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 502 ms: 1.07x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 47.3 ms: 1.08x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 103 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 57.2 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.23 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.7 ms: 1.14x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.81 us: 1.15x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 26.6 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.82 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 194 ns: 4.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (3): python_startup, sqlite_synth, coroutines
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 66.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x