# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.370x faster
- HPT reliability: 81.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| nbody          | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 42.0 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.97 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.3 ms: 1.09x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.6 ms: 1.07x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 95.0 us: 1.05x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.76 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.92 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pprint_pformat                   | 650 ms                                                         | 590 ns: 1101876.58x faster                                              |
| pprint_safe_repr                 | 322 ms                                                         | 344 ns: 935155.39x faster                                               |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 527 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 252 ms: 1.61x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 254 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                   |
| go                               | 72.6 ms                                                        | 57.1 ms: 1.27x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.13 us: 1.14x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 42.0 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 23.3 ms: 1.09x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.97 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 33.6 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                  |
| json_dumps                       | 4.65 ms                                                        | 4.41 ms: 1.05x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 95.0 us: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 954 us: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.6 us: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.92 ms: 1.01x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.84 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.00x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.62 ms: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.0 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.76 ms: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 212 ms: 1.02x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 39.0 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.27 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.2 ms: 1.06x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.5 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                   |
| pycparser                        | 470 ms                                                         | 512 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.29 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.80 us: 1.14x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.58 us: 1.16x slower                                                   |
| nbody                            | 42.5 ms                                                        | 49.2 ms: 1.16x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.9 ms: 1.16x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.10 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.25x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.79 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 198 ns: 4.89x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.33x faster                                                            |

Benchmark hidden because not significant (4): sqlite_synth, mako, asyncio_websockets, richards
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.370x faster

# HPT report

- Reliability score: 81.25% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x