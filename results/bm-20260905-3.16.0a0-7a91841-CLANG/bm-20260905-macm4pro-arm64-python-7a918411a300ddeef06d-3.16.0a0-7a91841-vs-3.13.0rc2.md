# Results vs. 3.13.0rc2

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.059x faster
- HPT reliability: 99.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 938 ms: 1.12x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                   |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 337 ms: 1.55x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 8.92 ms: 1.20x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 88.1 ms: 1.07x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 812 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 91.7 us: 1.08x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.59 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 519 ms: 2.04x faster                                                    |
| pylint                           | 106 ms                                                         | 56.2 ms: 1.88x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 310 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 337 ms: 1.55x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.10 ms: 1.53x faster                                                   |
| deepcopy                         | 145 us                                                         | 95.2 us: 1.52x faster                                                   |
| k_core                           | 1.46 sec                                                       | 982 ms: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.48x faster                                                   |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 48.1 ms: 1.33x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 48.8 us: 1.33x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 326 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 812 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 822 us: 1.21x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 8.92 ms: 1.20x faster                                                   |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                                   |
| docutils                         | 1.05 sec                                                       | 938 ms: 1.12x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.1 ms: 1.10x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 91.7 us: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 88.1 ms: 1.07x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.9 ms: 1.06x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.5 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.5 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.6 ms: 1.05x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 282 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.31 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.67 us: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.0 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.00x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 659 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.02x slower                                                    |
| connected_components             | 208 ms                                                         | 211 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.6 ms: 1.02x slower                                                   |
| generators                       | 15.7 ms                                                        | 16.1 ms: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 54.4 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.3 ns: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                   |
| nbody                            | 42.5 ms                                                        | 44.6 ms: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.5 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 115 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.84 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.59 ms: 1.11x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.4 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): pprint_safe_repr
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 99.20% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x