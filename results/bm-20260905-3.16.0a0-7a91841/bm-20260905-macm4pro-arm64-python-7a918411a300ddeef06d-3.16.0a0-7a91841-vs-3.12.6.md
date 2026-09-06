# Results vs. 3.12.6

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.147x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 939 ms: 1.09x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 312 ms: 1.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 336 ms: 1.33x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 281 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| nbody          | 54.2 ms                                                  | 42.6 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.59 ms: 1.18x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 821 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.2 ms: 1.03x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                   |
| python_startup         | 8.01 ms                                                  | 9.52 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.18x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.05 ms: 5.12x faster                                                   |
| pylint                           | 128 ms                                                   | 57.6 ms: 2.22x faster                                                   |
| mdp                              | 1.09 sec                                                 | 514 ms: 2.13x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.5 us: 1.66x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.60 us: 1.49x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 312 ms: 1.47x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.4 us: 1.47x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                   |
| go                               | 70.0 ms                                                  | 52.6 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 336 ms: 1.33x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.3 ms: 1.29x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                   |
| nbody                            | 54.2 ms                                                  | 42.6 ms: 1.27x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.26x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 48.9 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 34.9 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 281 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.59 ms: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 290 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 821 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.0 ms: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 975 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.66 ms: 1.14x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.0 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.09x faster                                                   |
| docutils                         | 1.02 sec                                                 | 939 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.6 ms: 1.09x faster                                                   |
| fannkuch                         | 176 ms                                                   | 162 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 302 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 622 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.92 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.04x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.8 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.2 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 813 us: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 490 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 421 us: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.52 ms: 1.19x slower                                                   |
| many_optionals                   | 195 us                                                   | 237 us: 1.22x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.20x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.147x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x