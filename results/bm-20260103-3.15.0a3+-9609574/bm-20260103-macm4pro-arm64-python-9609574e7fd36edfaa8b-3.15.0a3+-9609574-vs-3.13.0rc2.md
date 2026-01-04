# Results vs. 3.13.0rc2

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.7 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.8 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.7 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 915 ms: 1.09x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.8 us: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.68 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.30x faster                                                     |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.03 ms: 1.55x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.7 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 915 ms: 1.09x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 917 us: 1.08x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 301 ms: 1.07x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 611 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.1 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.68 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.8 us: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.1 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                     |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.46 us: 1.00x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.2 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.80 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 963 ns: 1.02x slower                                                     |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.0 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| nbody                            | 42.5 ms                                                        | 45.7 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.8 ms: 2.76x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (4): logging_simple, logging_silent, deltablue, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260103-3.15.0a3+-9609574/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x