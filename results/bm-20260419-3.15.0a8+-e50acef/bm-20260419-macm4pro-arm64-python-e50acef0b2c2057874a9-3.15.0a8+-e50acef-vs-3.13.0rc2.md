# Results vs. 3.13.0rc2

- fork: python
- ref: e50acef0b2c2057874a9
- machine: darwin-arm64
- commit hash: e50acef
- commit date: 2026-04-19
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.6 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.89 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| pylint                           | 106 ms                                                         | 50.9 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 230 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 895 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.8 us: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 52.9 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.35x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 102 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.3 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.9 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 958 us: 1.04x faster                                                     |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 635 ms: 1.02x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.76 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.7 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 5.89 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 64.1 us: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.8 us: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.4 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.48 ms: 1.01x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.6 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.03 us: 1.03x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.8 ms: 1.07x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.5 ms: 1.07x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.15x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.1 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.5 ms: 1.23x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.53 ms: 1.24x slower                                                    |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.6 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): logging_simple, python_startup, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260419-3.15.0a8+-e50acef/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x