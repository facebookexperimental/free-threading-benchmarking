# Results vs. 3.13.0rc2

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.171x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| html5lib       | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                    |
| sphinx         | 409 ms                                                         | 381 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 214 ms: 2.44x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 216 ms: 1.79x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 95.1 ms: 1.50x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 93.5 ms: 1.42x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 36.8 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.7 ms: 1.33x faster                                                    |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.41 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 661 ms: 1.51x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.21x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 83.2 us: 1.20x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 21.7 ms: 1.17x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 124 us: 1.05x faster                                                     |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.17x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.95 ms: 1.12x faster                                                    |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 212 ms: 2.48x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 214 ms: 2.44x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.27 ms: 2.38x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.1 ms: 2.22x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 218 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 572 ms: 1.85x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 216 ms: 1.79x faster                                                     |
| k_core                           | 1.46 sec                                                       | 859 ms: 1.70x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 39.0 ms: 1.64x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.82 ms: 1.64x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.3 us: 1.60x faster                                                    |
| go                               | 72.6 ms                                                        | 46.2 ms: 1.57x faster                                                    |
| deepcopy                         | 145 us                                                         | 92.5 us: 1.57x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 661 ms: 1.51x faster                                                     |
| pyflate                          | 222 ms                                                         | 148 ms: 1.50x faster                                                     |
| scimark_lu                       | 42.8 ms                                                        | 28.6 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 95.1 ms: 1.50x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 93.5 ms: 1.42x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 132 ms: 1.41x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.39x faster                                                     |
| float                            | 31.4 ms                                                        | 23.7 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 977 ns: 1.33x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.8 ms: 1.31x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 508 ms: 1.28x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 252 ms: 1.28x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.14 ms: 1.27x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 98.1 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.21x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 83.2 us: 1.20x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.57 ms: 1.19x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 36.8 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.17x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 19.8 ms: 1.17x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 21.7 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.82 sec: 1.17x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                    |
| fannkuch                         | 179 ms                                                         | 154 ms: 1.16x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 35.1 ns: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.41 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 888 us: 1.12x faster                                                     |
| mako                             | 4.41 ms                                                        | 3.95 ms: 1.12x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 39.3 ms: 1.11x faster                                                    |
| pycparser                        | 470 ms                                                         | 424 ms: 1.11x faster                                                     |
| chaos                            | 24.3 ms                                                        | 22.2 ms: 1.09x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.25 us: 1.09x faster                                                    |
| json                             | 1.94 ms                                                        | 1.80 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 381 ms: 1.07x faster                                                     |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 31.5 ms: 1.07x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.10 us: 1.07x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.29 us: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| shortest_path                    | 225 ms                                                         | 214 ms: 1.05x faster                                                     |
| pickle_pure_python               | 130 us                                                         | 124 us: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 35.8 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 933 ns: 1.02x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.01 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.74 ms: 1.01x slower                                                    |
| raytrace                         | 109 ms                                                         | 110 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.6 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.33 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.5 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 106 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 119 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.6 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                             |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-JIT/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.171x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x