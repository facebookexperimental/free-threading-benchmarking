# Results vs. 3.13.0rc2

- fork: python
- ref: 480edc1aae0f54e34d21
- machine: darwin-arm64
- commit hash: 480edc1
- commit date: 2026-04-12
- overall geometric mean: 1.071x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.3 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.85 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                     |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 911 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.5 us: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.9 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 827 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 250 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.2 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.07x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.2 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.3 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.0 ms: 1.04x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.8 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 961 us: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 631 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.6 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.81 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.85 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.06 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.4 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.2 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.45 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.3 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 83.3 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (6): pycparser, typing_runtime_protocols, chaos, sqlite_synth, json_loads, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260412-3.15.0a8+-480edc1/bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8+-480edc1.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x