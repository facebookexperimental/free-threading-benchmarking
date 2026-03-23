# Results vs. 3.13.0rc2

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: darwin-arm64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.027x faster
- HPT reliability: 62.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.20x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.0 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.7 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 832 ms: 1.20x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 106 us: 1.06x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.79 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.11 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 800 us: 2.55x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 237 ms: 2.20x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 504 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 604 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.03 ms: 1.56x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 104 us: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.5 ms: 1.22x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 788 ns: 1.20x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 832 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.98 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 457 ms: 1.03x faster                                                     |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 124 ms: 1.00x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 663 ms: 1.02x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.0 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.2 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 106 us: 1.06x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.0 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 40.6 ms: 1.09x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.9 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.8 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.9 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.9 us: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.79 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.3 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.5 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.11 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.23 us: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.1 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| coverage                         | 31.2 ms                                                        | 39.3 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.1 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 263 us: 1.31x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 44.4 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 574 us: 1.39x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.7 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 62.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x