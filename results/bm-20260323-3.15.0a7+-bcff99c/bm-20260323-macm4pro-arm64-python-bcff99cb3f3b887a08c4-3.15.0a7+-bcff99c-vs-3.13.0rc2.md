# Results vs. 3.13.0rc2

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: darwin-arm64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.069x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.7 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 857 ms: 1.17x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.84 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.68 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.36x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 225 ms: 2.33x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 899 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 100 us: 1.45x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 53.4 ms: 1.36x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.3 us: 1.34x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.0 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| float                            | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 857 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.2 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 919 us: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.7 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.4 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.9 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.68 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.0 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.20 us: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 520 ms: 1.01x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 941 ns: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.3 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.61 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.84 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.50 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.7 ms: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| thrift                           | 309 us                                                         | 322 us: 1.04x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 45.3 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.31 us: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.80 ms: 1.09x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.9 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 177 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.0 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.8 ms: 2.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (7): nqueens, pycparser, json_loads, pprint_pformat, logging_silent, pprint_safe_repr, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-macm4pro-arm64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x