# Results vs. 3.13.0rc2

- fork: python
- ref: 898e6b395e63ad7f8bbe
- machine: darwin-arm64
- commit hash: 898e6b3
- commit date: 2025-03-26
- overall geometric mean: 1.050x faster
- HPT reliability: 72.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 974 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 186 ms: 2.81x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 198 ms: 2.65x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 189 ms: 2.14x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 82.7 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.54x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.6 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.08 ms: 1.18x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 220 ms: 1.06x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.4 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 61.5 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 34.7 ms: 1.33x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 55.7 ms: 1.12x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.04 ms: 1.08x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.16 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| mako            | 4.41 ms                                                        | 5.43 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 186 ms: 2.81x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 198 ms: 2.65x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 457 us: 2.18x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 189 ms: 2.14x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 205 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 82.7 ms: 1.60x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 121 ms: 1.54x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 99.6 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 34.7 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 230 ms: 1.31x faster                                                     |
| go                               | 72.6 ms                                                        | 58.1 ms: 1.25x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 240 ms: 1.22x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 53.4 ms: 1.20x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.08 ms: 1.18x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 806 ns: 1.18x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 881 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                     |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 55.7 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| docutils                         | 1.05 sec                                                       | 974 ms: 1.07x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pycparser                        | 470 ms                                                         | 449 ms: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.8 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.00x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 2.92 ms: 1.03x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.10 sec: 1.04x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.87 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 39.6 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 337 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 685 ms: 1.05x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                    |
| shortest_path                    | 225 ms                                                         | 237 ms: 1.06x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 220 ms: 1.06x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 68.6 us: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.16 ms: 1.06x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.28 ms: 1.07x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.5 ms: 1.07x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.37 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.5 ms: 1.08x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.04 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                     |
| connected_components             | 208 ms                                                         | 229 ms: 1.10x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.9 ms: 1.15x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.89 us: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.7 ms: 1.18x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 50.6 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.25 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.3 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.43 ms: 1.23x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.25x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.39 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 583 us: 1.42x slower                                                     |
| nbody                            | 42.5 ms                                                        | 61.5 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.4 ms: 2.57x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-898e6b3-CLANG,NOGIL/bm-20250326-macm4pro-arm64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 72.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x