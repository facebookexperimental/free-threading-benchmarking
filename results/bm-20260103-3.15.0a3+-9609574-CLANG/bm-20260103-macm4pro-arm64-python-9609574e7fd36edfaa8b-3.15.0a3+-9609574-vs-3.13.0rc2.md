# Results vs. 3.13.0rc2

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.088x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.7 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 46.1 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 878 ms: 1.14x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.08x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 93.5 us: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.39x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 223 ms: 2.35x faster                                                     |
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 898 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.94 ms: 1.59x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.6 us: 1.46x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.23x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 186 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 249 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 878 ms: 1.14x faster                                                     |
| float                            | 31.4 ms                                                        | 28.1 ms: 1.12x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 43.5 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 32.6 ms: 1.10x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.7 ms: 1.09x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.8 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 932 us: 1.07x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 93.5 us: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| sphinx                           | 409 ms                                                         | 389 ms: 1.05x faster                                                     |
| generators                       | 15.7 ms                                                        | 15.0 ms: 1.05x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.22 ms: 1.04x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.2 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.7 us: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 632 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 39.6 ns: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 416 us: 1.01x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.6 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.5 ms: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.4 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.97 us: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.9 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.2 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.4 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 46.1 ms: 1.09x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.0 ms: 1.12x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (3): scimark_fft, logging_format, 2to3
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x