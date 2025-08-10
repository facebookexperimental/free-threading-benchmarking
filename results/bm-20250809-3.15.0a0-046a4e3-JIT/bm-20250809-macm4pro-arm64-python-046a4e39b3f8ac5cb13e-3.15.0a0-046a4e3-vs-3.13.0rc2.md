# Results vs. 3.13.0rc2

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.022x faster
- HPT reliability: 89.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.1 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.66 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 822 ms: 1.22x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 92.4 us: 1.08x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 254 ms: 2.05x faster                                                    |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                                   |
| go                               | 72.6 ms                                                        | 57.3 ms: 1.27x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.9 ms: 1.26x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.78 ms: 1.23x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 822 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 265 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.66 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 293 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 595 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.90 ms: 1.09x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 92.4 us: 1.08x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.92 ms: 1.05x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 944 us: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.1 ms: 1.04x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.2 ms: 1.04x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.6 ms: 1.04x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.9 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.01x faster                                                   |
| float                            | 31.4 ms                                                        | 31.1 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.56 ms: 1.00x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.3 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.6 ms: 1.02x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| connected_components             | 208 ms                                                         | 218 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                   |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.4 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.1 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.38 us: 1.09x slower                                                   |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.7 ms: 1.10x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 47.3 ms: 1.11x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.22x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| many_optionals                   | 200 us                                                         | 323 us: 1.61x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.2 ms: 2.74x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.8 ms: 3.00x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (6): sphinx, logging_silent, regex_compile, json, sqlite_synth, mako
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 89.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x