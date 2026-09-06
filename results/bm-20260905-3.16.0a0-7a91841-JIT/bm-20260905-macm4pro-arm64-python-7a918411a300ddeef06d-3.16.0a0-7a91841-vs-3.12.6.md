# Results vs. 3.12.6

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.260x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 923 ms: 1.11x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 302 ms: 1.59x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 290 ms: 1.58x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 317 ms: 1.41x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 165 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.81 ms: 1.38x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 166 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 37.5 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 285 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 98.8 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 32.0 ms: 1.69x faster                                                   |
| float          | 37.9 ms                                                  | 23.1 ms: 1.64x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.40x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 110 us: 1.27x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.36 ms: 1.27x faster                                                   |
| tomli_loads          | 957 ms                                                   | 767 ms: 1.25x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 83.9 us: 1.23x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 22.6 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.19x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.09 ms: 1.13x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.88 ms: 1.23x faster                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.73 ms: 5.56x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 10.8 ms: 2.35x faster                                                   |
| richards                         | 22.4 ms                                                  | 9.62 ms: 2.33x faster                                                   |
| pylint                           | 128 ms                                                   | 56.0 ms: 2.29x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 32.3 ms: 1.89x faster                                                   |
| mdp                              | 1.09 sec                                                 | 586 ms: 1.86x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.1 us: 1.80x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 32.0 ms: 1.70x faster                                                   |
| nbody                            | 54.2 ms                                                  | 32.0 ms: 1.69x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 30.8 ms: 1.67x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 5.92 us: 1.66x faster                                                   |
| deepcopy                         | 161 us                                                   | 98.0 us: 1.65x faster                                                   |
| float                            | 37.9 ms                                                  | 23.1 ms: 1.64x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 43.9 us: 1.62x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 302 ms: 1.59x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 290 ms: 1.58x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 1.74 us: 1.47x faster                                                   |
| pyflate                          | 216 ms                                                   | 147 ms: 1.47x faster                                                    |
| go                               | 70.0 ms                                                  | 48.0 ms: 1.46x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.18 ms: 1.46x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 97.3 ms: 1.46x faster                                                   |
| logging_format                   | 2.80 us                                                  | 1.93 us: 1.46x faster                                                   |
| raytrace                         | 145 ms                                                   | 99.7 ms: 1.45x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.45x faster                                                   |
| chaos                            | 28.9 ms                                                  | 20.2 ms: 1.43x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 30.8 ms: 1.41x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 317 ms: 1.41x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 165 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.81 ms: 1.38x faster                                                   |
| async_generators                 | 206 ms                                                   | 152 ms: 1.36x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 24.0 ms: 1.34x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 166 ms: 1.34x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 520 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 257 ms: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 110 us: 1.27x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.36 ms: 1.27x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.41 ms: 1.26x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 767 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.0 ms: 1.25x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 31.5 ms: 1.23x faster                                                   |
| mako                             | 4.77 ms                                                  | 3.88 ms: 1.23x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 83.9 us: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 37.5 ms: 1.21x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.85 sec: 1.21x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.72 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 285 ms: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.18x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 22.6 ms: 1.18x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                   |
| fannkuch                         | 176 ms                                                   | 150 ms: 1.17x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                   |
| docutils                         | 1.02 sec                                                 | 923 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.4 ms: 1.09x faster                                                   |
| sympy_str                        | 104 ms                                                   | 96.1 ms: 1.08x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 53.1 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.42 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                   |
| meteor_contest                   | 47.7 ms                                                  | 44.9 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 917 ns: 1.05x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.14 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.92 ms: 1.04x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 820 us: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| k_core                           | 1.12 sec                                                 | 1.14 sec: 1.02x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 427 us: 1.02x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.66 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.09 ms: 1.13x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                                   |
| many_optionals                   | 195 us                                                   | 228 us: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 150 ms: 1.33x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 98.8 ms: 3.07x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.260x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.23x