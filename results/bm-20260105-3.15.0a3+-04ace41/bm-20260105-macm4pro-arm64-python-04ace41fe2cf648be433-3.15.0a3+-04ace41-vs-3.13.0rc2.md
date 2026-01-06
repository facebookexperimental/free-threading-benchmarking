# Results vs. 3.13.0rc2

- fork: python
- ref: 04ace41fe2cf648be433
- machine: darwin-arm64
- commit hash: 04ace41
- commit date: 2026-01-05
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 843 ms: 1.19x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.63 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 901 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.42x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 48.1 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 843 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.3 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 167 ms: 1.07x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 942 us: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.1 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.63 ms: 1.04x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.00x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.24 us: 1.00x slower                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.46 us: 1.01x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 970 ns: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.91 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.05 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.4 ns: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.7 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.6 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.41 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.77 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.0 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): pycparser, json_loads, thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260105-3.15.0a3+-04ace41/bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x