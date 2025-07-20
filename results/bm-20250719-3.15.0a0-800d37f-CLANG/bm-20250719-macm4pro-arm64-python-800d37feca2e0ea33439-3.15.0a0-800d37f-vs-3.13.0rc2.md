# Results vs. 3.13.0rc2

- fork: python
- ref: 800d37feca2e0ea33439
- machine: darwin-arm64
- commit hash: 800d37f
- commit date: 2025-07-19
- overall geometric mean: 1.061x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.6 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 47.9 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 104 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 23.1 ms: 1.10x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.31 ms: 1.08x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 45.0 ms: 1.02x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 135 us: 1.03x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                   |
| genshi_text     | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                   |
| mako            | 4.41 ms                                                        | 4.52 ms: 1.02x slower                                                   |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                    |
| mdp                              | 1.06 sec                                                       | 509 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 246 ms: 1.57x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.8 us: 1.45x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.45x faster                                                   |
| go                               | 72.6 ms                                                        | 50.8 ms: 1.43x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 143 ms: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.8 ms: 1.26x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 806 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.3 ms: 1.15x faster                                                   |
| richards                         | 22.1 ms                                                        | 19.3 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.0 ms: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.54 ms: 1.12x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 38.6 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.11x faster                                                  |
| genshi_xml                       | 21.4 ms                                                        | 19.4 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 23.1 ms: 1.10x faster                                                   |
| generators                       | 15.7 ms                                                        | 14.3 ms: 1.09x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 32.8 ms: 1.09x faster                                                   |
| thrift                           | 309 us                                                         | 284 us: 1.09x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 59.6 us: 1.08x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.31 ms: 1.08x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| float                            | 31.4 ms                                                        | 29.3 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 93.5 us: 1.06x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 38.5 ns: 1.05x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 619 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.04x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.31 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.0 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 157 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                    |
| sympy_str                        | 95.5 ms                                                        | 94.8 ms: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 997 us: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 420 us: 1.02x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.52 ms: 1.02x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 53.6 ms: 1.02x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 6.98 us: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 170 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 135 us: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.14 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 46.0 ms: 1.05x slower                                                   |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.26 ms: 1.05x slower                                                   |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.7 ms: 1.06x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.95 ms: 1.10x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 104 ms: 1.10x slower                                                    |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.9 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.49 ms: 1.52x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (7): dask, sqlite_synth, docutils, asyncio_websockets, meteor_contest, json_loads, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250719-3.15.0a0-800d37f-CLANG/bm-20250719-macm4pro-arm64-python-800d37feca2e0ea33439-3.15.0a0-800d37f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x