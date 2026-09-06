# Results vs. base

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.000x slower
- HPT reliability: 60.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 117 ms                                                                                                            | 119 ms: 1.01x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io                    | 312 ms                                                                                                            | 308 ms: 1.01x faster                                                                                                    |
| asyncio_websockets               | 189 ms                                                                                                            | 190 ms: 1.00x slower                                                                                                    |
| asyncio_tcp_ssl                  | 535 ms                                                                                                            | 539 ms: 1.01x slower                                                                                                    |
| async_tree_eager_tg              | 103 ms                                                                                                            | 104 ms: 1.01x slower                                                                                                    |
| async_tree_eager_memoization     | 115 ms                                                                                                            | 116 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                                                            | 227 ms: 1.01x slower                                                                                                    |
| async_tree_eager                 | 40.0 ms                                                                                                           | 40.6 ms: 1.02x slower                                                                                                   |
| async_tree_eager_cpu_io_mixed_tg | 261 ms                                                                                                            | 266 ms: 1.02x slower                                                                                                    |
| coroutines                       | 9.41 ms                                                                                                           | 10.3 ms: 1.10x slower                                                                                                   |
| async_generators                 | 144 ms                                                                                                            | 180 ms: 1.25x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (11): async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_eager_io, async_tree_memoization, async_tree_eager_io_tg, async_tree_none, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_cpu_io_mixed, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 165 ms                                                                                                            | 164 ms: 1.01x faster                                                                                                    |
| float          | 28.7 ms                                                                                                           | 30.0 ms: 1.04x slower                                                                                                   |
| nbody          | 42.6 ms                                                                                                           | 44.6 ms: 1.05x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 91.6 ms                                                                                                           | 88.1 ms: 1.04x faster                                                                                                   |
| regex_v8       | 9.25 ms                                                                                                           | 8.92 ms: 1.04x faster                                                                                                   |
| regex_compile  | 54.2 ms                                                                                                           | 54.8 ms: 1.01x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 101 us                                                                                                            | 91.7 us: 1.10x faster                                                                                                   |
| xml_etree_iterparse  | 44.1 ms                                                                                                           | 41.2 ms: 1.07x faster                                                                                                   |
| xml_etree_generate   | 36.0 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                   |
| xml_etree_parse      | 66.2 ms                                                                                                           | 64.3 ms: 1.03x faster                                                                                                   |
| xml_etree_process    | 25.2 ms                                                                                                           | 24.5 ms: 1.03x faster                                                                                                   |
| pickle               | 6.21 us                                                                                                           | 6.08 us: 1.02x faster                                                                                                   |
| pickle_pure_python   | 141 us                                                                                                            | 139 us: 1.01x faster                                                                                                    |
| tomli_loads          | 821 ms                                                                                                            | 812 ms: 1.01x faster                                                                                                    |
| json_dumps           | 3.59 ms                                                                                                           | 3.57 ms: 1.01x faster                                                                                                   |
| unpickle_list        | 2.02 us                                                                                                           | 2.05 us: 1.02x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (4): pickle_list, pickle_dict, unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 9.52 ms                                                                                                           | 9.05 ms: 1.05x faster                                                                                                   |
| python_startup_no_site | 6.72 ms                                                                                                           | 6.59 ms: 1.02x faster                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.04x faster                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 14.9 ms                                                                                                           | 14.7 ms: 1.01x faster                                                                                                   |
| mako            | 4.56 ms                                                                                                           | 4.84 ms: 1.06x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.02x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-CLANG/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python             | 101 us                                                                                                            | 91.7 us: 1.10x faster                                                                                                   |
| xml_etree_iterparse              | 44.1 ms                                                                                                           | 41.2 ms: 1.07x faster                                                                                                   |
| generators                       | 17.2 ms                                                                                                           | 16.1 ms: 1.07x faster                                                                                                   |
| deepcopy_memo                    | 11.8 us                                                                                                           | 11.2 us: 1.06x faster                                                                                                   |
| xml_etree_generate               | 36.0 ms                                                                                                           | 34.2 ms: 1.05x faster                                                                                                   |
| deepcopy_reduce                  | 1.08 us                                                                                                           | 1.03 us: 1.05x faster                                                                                                   |
| python_startup                   | 9.52 ms                                                                                                           | 9.05 ms: 1.05x faster                                                                                                   |
| raytrace                         | 121 ms                                                                                                            | 115 ms: 1.05x faster                                                                                                    |
| scimark_lu                       | 49.8 ms                                                                                                           | 47.4 ms: 1.05x faster                                                                                                   |
| regex_dna                        | 91.6 ms                                                                                                           | 88.1 ms: 1.04x faster                                                                                                   |
| thrift                           | 311 us                                                                                                            | 300 us: 1.04x faster                                                                                                    |
| regex_v8                         | 9.25 ms                                                                                                           | 8.92 ms: 1.04x faster                                                                                                   |
| unpack_sequence                  | 23.5 ns                                                                                                           | 22.7 ns: 1.04x faster                                                                                                   |
| bench_thread_pool                | 421 us                                                                                                            | 408 us: 1.03x faster                                                                                                    |
| xml_etree_parse                  | 66.2 ms                                                                                                           | 64.3 ms: 1.03x faster                                                                                                   |
| xml_etree_process                | 25.2 ms                                                                                                           | 24.5 ms: 1.03x faster                                                                                                   |
| sqlglot_v2_optimize              | 22.2 ms                                                                                                           | 21.6 ms: 1.03x faster                                                                                                   |
| deepcopy                         | 97.5 us                                                                                                           | 95.2 us: 1.02x faster                                                                                                   |
| sqlglot_v2_transpile             | 620 us                                                                                                            | 605 us: 1.02x faster                                                                                                    |
| pyflate                          | 190 ms                                                                                                            | 186 ms: 1.02x faster                                                                                                    |
| sqlglot_v2_normalize             | 45.5 ms                                                                                                           | 44.4 ms: 1.02x faster                                                                                                   |
| pickle                           | 6.21 us                                                                                                           | 6.08 us: 1.02x faster                                                                                                   |
| sqlglot_v2_parse                 | 505 us                                                                                                            | 495 us: 1.02x faster                                                                                                    |
| python_startup_no_site           | 6.72 ms                                                                                                           | 6.59 ms: 1.02x faster                                                                                                   |
| crypto_pyaes                     | 38.0 ms                                                                                                           | 37.3 ms: 1.02x faster                                                                                                   |
| sympy_integrate                  | 7.45 ms                                                                                                           | 7.31 ms: 1.02x faster                                                                                                   |
| sympy_expand                     | 169 ms                                                                                                            | 166 ms: 1.02x faster                                                                                                    |
| sympy_str                        | 99.4 ms                                                                                                           | 97.6 ms: 1.02x faster                                                                                                   |
| telco                            | 2.90 ms                                                                                                           | 2.85 ms: 1.02x faster                                                                                                   |
| scimark_sor                      | 48.9 ms                                                                                                           | 48.1 ms: 1.02x faster                                                                                                   |
| sympy_sum                        | 55.2 ms                                                                                                           | 54.4 ms: 1.01x faster                                                                                                   |
| pickle_pure_python               | 141 us                                                                                                            | 139 us: 1.01x faster                                                                                                    |
| pycparser                        | 490 ms                                                                                                            | 484 ms: 1.01x faster                                                                                                    |
| async_tree_io                    | 312 ms                                                                                                            | 308 ms: 1.01x faster                                                                                                    |
| django_template                  | 14.9 ms                                                                                                           | 14.7 ms: 1.01x faster                                                                                                   |
| tomli_loads                      | 821 ms                                                                                                            | 812 ms: 1.01x faster                                                                                                    |
| pathlib                          | 10.7 ms                                                                                                           | 10.6 ms: 1.01x faster                                                                                                   |
| json_dumps                       | 3.59 ms                                                                                                           | 3.57 ms: 1.01x faster                                                                                                   |
| logging_format                   | 2.39 us                                                                                                           | 2.37 us: 1.01x faster                                                                                                   |
| go                               | 52.6 ms                                                                                                           | 52.2 ms: 1.01x faster                                                                                                   |
| pidigits                         | 165 ms                                                                                                            | 164 ms: 1.01x faster                                                                                                    |
| deltablue                        | 1.47 ms                                                                                                           | 1.46 ms: 1.00x faster                                                                                                   |
| hexiom                           | 2.66 ms                                                                                                           | 2.66 ms: 1.00x faster                                                                                                   |
| scimark_fft                      | 123 ms                                                                                                            | 123 ms: 1.00x slower                                                                                                    |
| asyncio_websockets               | 189 ms                                                                                                            | 190 ms: 1.00x slower                                                                                                    |
| typing_runtime_protocols         | 48.4 us                                                                                                           | 48.8 us: 1.01x slower                                                                                                   |
| asyncio_tcp_ssl                  | 535 ms                                                                                                            | 539 ms: 1.01x slower                                                                                                    |
| many_optionals                   | 237 us                                                                                                            | 239 us: 1.01x slower                                                                                                    |
| async_tree_eager_tg              | 103 ms                                                                                                            | 104 ms: 1.01x slower                                                                                                    |
| gc_traversal                     | 1.92 ms                                                                                                           | 1.94 ms: 1.01x slower                                                                                                   |
| 2to3                             | 117 ms                                                                                                            | 119 ms: 1.01x slower                                                                                                    |
| comprehensions                   | 6.60 us                                                                                                           | 6.67 us: 1.01x slower                                                                                                   |
| create_gc_cycles                 | 813 us                                                                                                            | 822 us: 1.01x slower                                                                                                    |
| subparsers                       | 4.05 ms                                                                                                           | 4.10 ms: 1.01x slower                                                                                                   |
| mdp                              | 514 ms                                                                                                            | 519 ms: 1.01x slower                                                                                                    |
| regex_compile                    | 54.2 ms                                                                                                           | 54.8 ms: 1.01x slower                                                                                                   |
| async_tree_eager_memoization     | 115 ms                                                                                                            | 116 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                                                            | 227 ms: 1.01x slower                                                                                                    |
| bpe_tokeniser                    | 1.96 sec                                                                                                          | 1.99 sec: 1.01x slower                                                                                                  |
| scimark_monte_carlo              | 28.0 ms                                                                                                           | 28.5 ms: 1.01x slower                                                                                                   |
| nqueens                          | 34.9 ms                                                                                                           | 35.5 ms: 1.02x slower                                                                                                   |
| async_tree_eager                 | 40.0 ms                                                                                                           | 40.6 ms: 1.02x slower                                                                                                   |
| richards_super                   | 23.2 ms                                                                                                           | 23.6 ms: 1.02x slower                                                                                                   |
| async_tree_eager_cpu_io_mixed_tg | 261 ms                                                                                                            | 266 ms: 1.02x slower                                                                                                    |
| unpickle_list                    | 2.02 us                                                                                                           | 2.05 us: 1.02x slower                                                                                                   |
| spectral_norm                    | 42.3 ms                                                                                                           | 43.0 ms: 1.02x slower                                                                                                   |
| logging_silent                   | 41.5 ns                                                                                                           | 42.3 ns: 1.02x slower                                                                                                   |
| shortest_path                    | 223 ms                                                                                                            | 229 ms: 1.02x slower                                                                                                    |
| connected_components             | 206 ms                                                                                                            | 211 ms: 1.03x slower                                                                                                    |
| richards                         | 20.4 ms                                                                                                           | 20.9 ms: 1.03x slower                                                                                                   |
| float                            | 28.7 ms                                                                                                           | 30.0 ms: 1.04x slower                                                                                                   |
| nbody                            | 42.6 ms                                                                                                           | 44.6 ms: 1.05x slower                                                                                                   |
| scimark_sparse_mat_mult          | 1.82 ms                                                                                                           | 1.92 ms: 1.05x slower                                                                                                   |
| pprint_pformat                   | 622 ms                                                                                                            | 659 ms: 1.06x slower                                                                                                    |
| mako                             | 4.56 ms                                                                                                           | 4.84 ms: 1.06x slower                                                                                                   |
| pprint_safe_repr                 | 302 ms                                                                                                            | 321 ms: 1.06x slower                                                                                                    |
| coroutines                       | 9.41 ms                                                                                                           | 10.3 ms: 1.10x slower                                                                                                   |
| fannkuch                         | 162 ms                                                                                                            | 181 ms: 1.12x slower                                                                                                    |
| async_generators                 | 144 ms                                                                                                            | 180 ms: 1.25x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (28): pylint, async_tree_none_tg, sphinx, html5lib, async_tree_io_tg, async_tree_memoization_tg, pickle_list, docutils, logging_simple, pickle_dict, async_tree_eager_io, chaos, async_tree_memoization, bench_mp_pool, meteor_contest, async_tree_eager_io_tg, dulwich_log, async_tree_none, unpickle, sqlite_synth, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_cpu_io_mixed, json_loads, k_core, async_tree_eager_memoization_tg, json, regex_effbot

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 60.82% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x