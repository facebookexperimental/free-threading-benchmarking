# Results vs. 3.13.0rc2

- fork: python
- ref: 5b5ee3c4bf1a28b61063
- machine: darwin-arm64
- commit hash: 5b5ee3c
- commit date: 2025-12-23
- overall geometric mean: 1.013x faster
- HPT reliability: 55.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 427 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.9 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 983 ms: 1.02x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.87 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.47 ms: 1.24x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 808 us: 2.52x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.11x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 503 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.55x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.2 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 983 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 332 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 427 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 107 us: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.7 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.6 ms: 1.09x slower                                                    |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.4 ns: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.7 us: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.72 us: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.87 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.6 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.12 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.16 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.9 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.27 us: 1.22x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.47 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 128 ms: 1.25x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.6 ms: 1.31x slower                                                    |
| many_optionals                   | 200 us                                                         | 266 us: 1.33x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 549 us: 1.33x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 58.0 ms: 1.36x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.9 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251223-3.15.0a3+-5b5ee3c-NOGIL/bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3+-5b5ee3c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 55.46% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x