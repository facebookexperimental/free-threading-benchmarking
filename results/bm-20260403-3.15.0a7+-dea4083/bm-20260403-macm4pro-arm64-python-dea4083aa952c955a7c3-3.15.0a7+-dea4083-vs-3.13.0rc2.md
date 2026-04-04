# Results vs. 3.13.0rc2

- fork: python
- ref: dea4083aa952c955a7c3
- machine: darwin-arm64
- commit hash: dea4083
- commit date: 2026-04-03
- overall geometric mean: 1.071x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.2 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.7 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.8 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.83 ms: 1.01x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 540 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 100 us: 1.45x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| go                               | 72.6 ms                                                        | 52.8 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.2 ms: 1.35x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.8 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 825 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.19x faster                                                    |
| float                            | 31.4 ms                                                        | 26.9 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.5 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.07x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.6 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 949 us: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.2 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.8 us: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.83 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 318 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 644 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 942 ns: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.51 ms: 1.00x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.4 ms: 1.00x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.8 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.03x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.3 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.29 us: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.9 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.41 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.7 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): pycparser, json, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260403-3.15.0a7+-dea4083/bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x