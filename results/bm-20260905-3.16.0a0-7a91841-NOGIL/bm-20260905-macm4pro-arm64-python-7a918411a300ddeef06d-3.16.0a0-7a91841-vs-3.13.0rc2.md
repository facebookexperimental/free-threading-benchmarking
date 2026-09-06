# Results vs. 3.13.0rc2

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.060x slower
- HPT reliability: 99.51%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 409 ms                                                         | 456 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 309 ms: 1.31x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 53.0 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 279 ms: 1.34x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 166 ms: 1.62x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 35.5 ms: 1.13x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.9 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 69.6 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.8 ms: 1.11x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.3 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 165 us: 1.27x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.44 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| django_template | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.39x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 780 us: 2.62x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 492 us: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 54.3 ms: 1.94x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 307 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 306 ms: 1.70x faster                                                    |
| mdp                              | 1.06 sec                                                       | 633 ms: 1.67x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.43x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.60 ms: 1.36x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 309 ms: 1.31x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.73 ms: 1.25x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 317 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 802 ns: 1.18x faster                                                    |
| deepcopy                         | 145 us                                                         | 123 us: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| go                               | 72.6 ms                                                        | 66.9 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 61.1 us: 1.06x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.6 us: 1.05x faster                                                   |
| pyflate                          | 222 ms                                                         | 211 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 973 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 63.0 ms: 1.02x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 495 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.07x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 137 ms: 1.11x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.8 ms: 1.11x slower                                                   |
| sphinx                           | 409 ms                                                         | 456 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 53.9 ms: 1.13x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.48 ms: 1.13x slower                                                   |
| float                            | 31.4 ms                                                        | 35.5 ms: 1.13x slower                                                   |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| thrift                           | 309 us                                                         | 363 us: 1.18x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.63 us: 1.18x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 380 ms: 1.18x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.2 ms: 1.19x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 774 ms: 1.19x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.7 ms: 1.19x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.92 us: 1.19x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 52.3 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 62.9 ms: 1.20x slower                                                   |
| richards                         | 22.1 ms                                                        | 26.6 ms: 1.21x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.21x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 30.3 ms: 1.23x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 53.0 ms: 1.23x slower                                                   |
| 2to3                             | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.19 ms: 1.23x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 197 ms: 1.23x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 31.3 ms: 1.24x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.44 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.60 ms: 1.26x slower                                                   |
| chaos                            | 24.3 ms                                                        | 30.7 ms: 1.27x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 165 us: 1.27x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 52.4 ns: 1.29x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.87 us: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.90 ms: 1.34x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.8 ms: 1.34x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 279 ms: 1.34x slower                                                    |
| raytrace                         | 109 ms                                                         | 147 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.02 ms: 1.39x slower                                                   |
| django_template                  | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 69.6 ms: 1.45x slower                                                   |
| nbody                            | 42.5 ms                                                        | 62.9 ms: 1.48x slower                                                   |
| generators                       | 15.7 ms                                                        | 24.6 ms: 1.57x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 166 ms: 1.62x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 69.6 ms: 1.63x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.11x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, deepcopy_reduce
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841-NOGIL/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 99.51% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.27x