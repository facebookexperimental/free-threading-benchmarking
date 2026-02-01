# Results vs. 3.13.0rc2

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 106 ms: 1.05x faster                                                     |
| docutils       | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.6 ms: 1.13x faster                                                    |
| sphinx         | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 210 ms: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 215 ms: 1.80x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 96.6 ms: 1.47x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 93.0 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 240 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.4 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.8 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 42.9 ms: 1.12x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 773 ms: 1.29x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.71 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 32.2 ms: 1.11x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.0 ms: 1.10x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 91.5 us: 1.09x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.2 ms: 1.11x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 9.00 ms: 1.11x faster                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 210 ms: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 211 ms: 2.46x faster                                                     |
| mdp                              | 1.06 sec                                                       | 513 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 215 ms: 1.80x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.75 ms: 1.67x faster                                                    |
| k_core                           | 1.46 sec                                                       | 895 ms: 1.63x faster                                                     |
| deepcopy                         | 145 us                                                         | 92.0 us: 1.58x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 96.6 ms: 1.47x faster                                                    |
| go                               | 72.6 ms                                                        | 50.4 ms: 1.44x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 93.0 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.6 ms: 1.32x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 990 ns: 1.31x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 773 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 240 ms: 1.26x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.71 ms: 1.26x faster                                                    |
| pyflate                          | 222 ms                                                         | 184 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.5 ms: 1.17x faster                                                    |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.2 ms: 1.15x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.6 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.12x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 884 us: 1.12x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.4 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 42.9 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.12x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 19.2 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.2 ms: 1.11x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.00 ms: 1.11x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.0 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 91.5 us: 1.09x faster                                                    |
| generators                       | 15.7 ms                                                        | 14.5 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 299 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                     |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 980 ms: 1.07x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 610 ms: 1.07x faster                                                     |
| pidigits                         | 166 ms                                                         | 156 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.09 ms: 1.06x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.31 us: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.2 us: 1.06x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| thrift                           | 309 us                                                         | 294 us: 1.05x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.38 ms: 1.05x faster                                                    |
| 2to3                             | 112 ms                                                         | 106 ms: 1.05x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.8 ms: 1.04x faster                                                    |
| pycparser                        | 470 ms                                                         | 453 ms: 1.04x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.2 ns: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| meteor_contest                   | 47.9 ms                                                        | 47.2 ms: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| coverage                         | 31.2 ms                                                        | 30.9 ms: 1.01x faster                                                    |
| fannkuch                         | 179 ms                                                         | 178 ms: 1.01x faster                                                     |
| sympy_str                        | 95.5 ms                                                        | 95.0 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| sympy_expand                     | 159 ms                                                         | 160 ms: 1.00x slower                                                     |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 415 us: 1.01x slower                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.3 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.01x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.01x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.93 us: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.6 ms: 1.02x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| pylint                           | 106 ms                                                         | 109 ms: 1.03x slower                                                     |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.18 ms: 1.04x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.8 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 117 ms: 1.14x slower                                                     |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (3): spectral_norm, sympy_sum, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260130-3.15.0a5+-ccbe41e-CLANG/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x