# Results vs. 3.13.0rc2

- fork: python
- ref: 78b1370de96bab5eee82
- machine: darwin-arm64
- commit hash: 78b1370
- commit date: 2026-01-19
- overall geometric mean: 1.039x faster
- HPT reliability: 79.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.6 ms: 3.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.1 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 872 ms: 1.15x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.50 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 763 us: 2.68x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 238 ms: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 489 us: 2.03x faster                                                     |
| mdp                              | 1.06 sec                                                       | 591 ms: 1.79x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 241 ms: 1.68x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.98 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 105 us: 1.39x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.2 us: 1.35x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 141 ms: 1.32x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| go                               | 72.6 ms                                                        | 59.0 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.9 ms: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 189 ms: 1.17x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 809 ns: 1.17x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.15x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 872 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 969 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 183 ms: 1.06x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| pycparser                        | 470 ms                                                         | 453 ms: 1.04x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.96 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.1 ms: 1.03x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.6 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.7 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.04x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.91 ms: 1.05x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.7 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.1 ns: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.61 us: 1.07x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.9 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 69.9 us: 1.08x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.57 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.13x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.3 ms: 1.13x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.1 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 183 ms: 1.15x slower                                                     |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.05 ms: 1.15x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.00 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.10 us: 1.19x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.3 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                     |
| coverage                         | 31.2 ms                                                        | 38.3 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.50 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.1 ms: 1.28x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.3 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 564 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.6 ms: 3.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): coroutines, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260119-3.15.0a5+-78b1370-NOGIL/bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5+-78b1370.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 79.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x