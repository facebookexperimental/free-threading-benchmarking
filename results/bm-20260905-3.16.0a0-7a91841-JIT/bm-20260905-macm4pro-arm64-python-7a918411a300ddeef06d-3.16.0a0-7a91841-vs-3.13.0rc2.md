# Results vs. 3.13.0rc2

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 923 ms: 1.13x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| sphinx         | 409 ms                                                         | 393 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 317 ms: 1.64x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 290 ms: 1.33x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 37.5 ms: 1.15x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 165 ms: 1.13x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 166 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.81 ms: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 98.8 ms: 3.42x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.1 ms: 1.36x faster                                                   |
| nbody          | 42.5 ms                                                        | 32.0 ms: 1.33x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.4 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                          | 1.11x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.36 ms: 1.38x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 767 ms: 1.30x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 83.9 us: 1.19x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 110 us: 1.18x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 22.6 ms: 1.12x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.61 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.88 ms: 1.14x faster                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                         | 22.1 ms                                                        | 9.62 ms: 2.29x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 10.8 ms: 2.28x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 32.3 ms: 1.98x faster                                                   |
| pylint                           | 106 ms                                                         | 56.0 ms: 1.89x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                    |
| mdp                              | 1.06 sec                                                       | 586 ms: 1.81x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.73 ms: 1.68x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 317 ms: 1.64x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.1 us: 1.62x faster                                                   |
| pyflate                          | 222 ms                                                         | 147 ms: 1.51x faster                                                    |
| go                               | 72.6 ms                                                        | 48.0 ms: 1.51x faster                                                   |
| deepcopy                         | 145 us                                                         | 98.0 us: 1.48x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 43.9 us: 1.47x faster                                                   |
| scimark_lu                       | 42.8 ms                                                        | 30.8 ms: 1.39x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.36 ms: 1.38x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 32.0 ms: 1.37x faster                                                   |
| float                            | 31.4 ms                                                        | 23.1 ms: 1.36x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 290 ms: 1.33x faster                                                    |
| nbody                            | 42.5 ms                                                        | 32.0 ms: 1.33x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 767 ms: 1.30x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.14 sec: 1.29x faster                                                  |
| logging_simple                   | 2.24 us                                                        | 1.74 us: 1.28x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 97.3 ms: 1.27x faster                                                   |
| logging_format                   | 2.45 us                                                        | 1.93 us: 1.27x faster                                                   |
| async_generators                 | 193 ms                                                         | 152 ms: 1.27x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 257 ms: 1.25x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 520 ms: 1.25x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 24.0 ms: 1.24x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.18 ms: 1.23x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 820 us: 1.21x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 30.8 ms: 1.21x faster                                                   |
| chaos                            | 24.3 ms                                                        | 20.2 ms: 1.20x faster                                                   |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 83.9 us: 1.19x faster                                                   |
| pickle_pure_python               | 130 us                                                         | 110 us: 1.18x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.41 ms: 1.18x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 17.0 ms: 1.16x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.66 ms: 1.15x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 37.5 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.85 sec: 1.15x faster                                                  |
| comprehensions                   | 6.80 us                                                        | 5.92 us: 1.15x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| mako                             | 4.41 ms                                                        | 3.88 ms: 1.14x faster                                                   |
| docutils                         | 1.05 sec                                                       | 923 ms: 1.13x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 165 ms: 1.13x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.6 ms: 1.12x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 166 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.81 ms: 1.10x faster                                                   |
| raytrace                         | 109 ms                                                         | 99.7 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 274 ms: 1.07x faster                                                    |
| json                             | 1.94 ms                                                        | 1.81 ms: 1.07x faster                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 31.5 ms: 1.07x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 44.9 ms: 1.07x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.92 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                   |
| sphinx                           | 409 ms                                                         | 393 ms: 1.04x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.4 ms: 1.04x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 917 ns: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.72 ms: 1.03x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                   |
| connected_components             | 208 ms                                                         | 203 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.42 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 96.1 ms: 1.01x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.1 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.61 ms: 1.11x slower                                                   |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 150 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 98.8 ms: 3.42x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                            |

Benchmark hidden because not significant (1): sympy_expand
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.18x