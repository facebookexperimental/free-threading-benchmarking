# Results vs. 3.13.0rc2

- fork: python
- ref: 78b1370de96bab5eee82
- machine: darwin-arm64
- commit hash: 78b1370
- commit date: 2026-01-19
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 382 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.9 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 94.1 us: 1.06x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.50 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.39x faster                                                     |
| mdp                              | 1.06 sec                                                       | 527 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| k_core                           | 1.46 sec                                                       | 894 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.1 us: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| go                               | 72.6 ms                                                        | 51.0 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.9 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 180 ms: 1.23x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 820 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| float                            | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.5 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.0 ms: 1.12x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 899 us: 1.11x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.1 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.8 ms: 1.09x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 166 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| sphinx                           | 409 ms                                                         | 382 ms: 1.07x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 61.0 us: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 94.1 us: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.70 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 617 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.50 ms: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 449 ms: 1.05x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.24 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 298 us: 1.04x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.4 ns: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.00 ms: 1.02x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.3 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.5 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.92 us: 1.02x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 53.7 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.1 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 35.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.1 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.9 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                    |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.5 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                             |

Benchmark hidden because not significant (3): coverage, sqlite_synth, meteor_contest
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260119-3.15.0a5+-78b1370/bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x