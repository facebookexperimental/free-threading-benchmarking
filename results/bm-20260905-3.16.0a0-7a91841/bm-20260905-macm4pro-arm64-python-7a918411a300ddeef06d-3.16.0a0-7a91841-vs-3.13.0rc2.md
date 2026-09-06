# Results vs. 3.13.0rc2

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.060x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 939 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 336 ms: 1.55x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 281 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.59 ms: 1.29x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 821 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.2 ms: 1.06x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.52 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| pylint                           | 106 ms                                                         | 57.6 ms: 1.83x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 336 ms: 1.55x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.05 ms: 1.54x faster                                                   |
| k_core                           | 1.46 sec                                                       | 975 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.5 us: 1.49x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                   |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.4 us: 1.33x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 48.9 ms: 1.31x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.59 ms: 1.29x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 312 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.23x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 813 us: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 821 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.19x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.25 ms: 1.16x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                   |
| docutils                         | 1.05 sec                                                       | 939 ms: 1.11x faster                                                    |
| fannkuch                         | 179 ms                                                         | 162 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.0 ms: 1.07x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 34.9 ms: 1.07x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.92 ms: 1.06x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 281 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.1 ms: 1.04x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 622 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 290 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.3 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.6 ms: 1.03x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.60 us: 1.03x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 311 us: 1.00x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 421 us: 1.02x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.56 ms: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.4 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.2 ms: 1.06x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.09x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.52 ms: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.2 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.16x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 153 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 103 ms: 3.55x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, nbody
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x