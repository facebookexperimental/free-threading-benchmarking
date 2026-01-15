# Results vs. 3.13.0rc2

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: darwin-arm64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.072x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.1 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.2 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 838 ms: 1.19x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| xml_etree_generate  | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                    |
| pickle_pure_python  | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.67 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| mdp                              | 1.06 sec                                                       | 545 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.8 us: 1.45x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.28x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 838 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.3 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.63 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 626 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.2 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.67 ms: 1.03x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 964 us: 1.03x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.1 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.10 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.8 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.1 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (4): unpickle_pure_python, scimark_sparse_mat_mult, sympy_integrate, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a5+-b8e925b/bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x