# Results vs. 3.13.0rc2

- fork: python
- ref: dc12d1999b88e84d5a6b
- machine: darwin-arm64
- commit hash: dc12d19
- commit date: 2026-03-03
- overall geometric mean: 1.060x faster
- HPT reliability: 97.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.86 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.7 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| mdp                              | 1.06 sec                                                       | 551 ms: 1.92x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 906 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 100 us: 1.45x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| go                               | 72.6 ms                                                        | 55.5 ms: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 897 us: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.86 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.7 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.23 us: 1.00x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 37.5 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.63 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 65.6 us: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 660 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.83 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 320 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.3 ms: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.3 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 43.1 ns: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.34 us: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.79 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.0 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 117 ms: 1.10x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| nbody                            | 42.5 ms                                                        | 48.0 ms: 1.13x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 48.4 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.2 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| generators                       | 15.7 ms                                                        | 20.5 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.2 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (5): sqlite_synth, coroutines, regex_dna, spectral_norm, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260303-3.15.0a6+-dc12d19/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6+-dc12d19.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 97.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.19x