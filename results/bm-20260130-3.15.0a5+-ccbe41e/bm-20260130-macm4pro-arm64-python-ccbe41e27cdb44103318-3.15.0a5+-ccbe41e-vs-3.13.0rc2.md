# Results vs. 3.13.0rc2

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 991 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 409 ms                                                         | 382 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.8 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 816 ms: 1.23x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.4 us: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 136 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.94 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 96.2 us: 1.51x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 51.6 ms: 1.41x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.8 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.3 ms: 1.32x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 816 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.84 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 103 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 879 us: 1.13x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.6 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 27.9 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.9 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.11x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.0 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.6 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| sphinx                           | 409 ms                                                         | 382 ms: 1.07x faster                                                     |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.06x faster                                                     |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                     |
| docutils                         | 1.05 sec                                                       | 991 ms: 1.06x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 616 ms: 1.05x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.0 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.1 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 95.4 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 452 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.38 us: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.98 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 301 us: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.01x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 36.9 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.62 ms: 1.00x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.1 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.54 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.8 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.03 us: 1.03x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.1 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 136 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.06x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (4): sqlite_synth, coverage, logging_silent, shortest_path
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260130-3.15.0a5+-ccbe41e/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x