# Results vs. 3.13.0rc2

- fork: python
- ref: acab53212d89b298ba0d
- machine: darwin-arm64
- commit hash: acab532
- commit date: 2026-11-10
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| docutils       | 1.05 sec                                                       | 918 ms: 1.14x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                       |
| sphinx         | 409 ms                                                         | 392 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                        |
| async_generators                 | 193 ms                                                         | 99.2 ms: 1.95x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 280 ms: 1.45x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 274 ms: 1.41x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 159 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.61 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| nbody          | 42.5 ms                                                        | 41.7 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                       |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 838 ms: 1.19x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 90.8 us: 1.10x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 66.3 ms: 1.06x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.24 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                                       |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 505 ms: 2.09x faster                                                        |
| pylint                           | 106 ms                                                         | 51.2 ms: 2.06x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                        |
| async_generators                 | 193 ms                                                         | 99.2 ms: 1.95x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.87x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.99 ms: 1.57x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 643 us: 1.54x faster                                                        |
| deepcopy                         | 145 us                                                         | 96.6 us: 1.50x faster                                                       |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 280 ms: 1.45x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.0 us: 1.44x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 274 ms: 1.41x faster                                                        |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.40x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.38x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.5 ms: 1.32x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                       |
| pyflate                          | 222 ms                                                         | 181 ms: 1.22x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 838 ms: 1.19x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 159 ms: 1.17x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                       |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.1 ms: 1.14x faster                                                       |
| docutils                         | 1.05 sec                                                       | 918 ms: 1.14x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 109 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.81 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.61 ms: 1.12x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                       |
| pidigits                         | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 90.8 us: 1.10x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.4 ms: 1.08x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.3 ms: 1.06x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.24 ms: 1.05x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.70 ms: 1.04x faster                                                       |
| sphinx                           | 409 ms                                                         | 392 ms: 1.04x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.03x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 924 ns: 1.03x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 314 ms: 1.03x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.6 us: 1.02x faster                                                       |
| nbody                            | 42.5 ms                                                        | 41.7 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.02x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.37 ms: 1.01x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 647 ms: 1.00x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.79 us: 1.00x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x slower                                                       |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                        |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                       |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 42.3 ns: 1.04x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                       |
| regex_dna                        | 94.6 ms                                                        | 99.0 ms: 1.05x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 45.0 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 66.3 ms: 1.06x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                       |
| many_optionals                   | 200 us                                                         | 234 us: 1.17x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmark hidden because not significant (2): connected_components, pycparser
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261110-3.16.0a2+dev-acab532/bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2+dev-acab532.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x