# Results vs. 3.13.0rc2

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: darwin-arm64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.030x faster
- HPT reliability: 76.54%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| sphinx         | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.74x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.1 ms: 1.32x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.18 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 851 ms: 1.17x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 106 us: 1.07x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.74 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.7 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 806 us: 2.53x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 509 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 596 ms: 1.78x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.74x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 244 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.09 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 103 us: 1.40x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.32x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.2 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 791 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.3 ms: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 851 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.18 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.6 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                     |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.1 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 456 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.99 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 123 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 657 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 415 ms: 1.02x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.5 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.8 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 106 us: 1.07x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.0 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                    |
| thrift                           | 309 us                                                         | 332 us: 1.07x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 43.7 ns: 1.08x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.7 ms: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.10 ms: 1.09x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.74 ms: 1.13x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.2 us: 1.13x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.15x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.06 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.7 ms: 1.16x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 186 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.07 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.13 us: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.2 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.1 ms: 1.32x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.33x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.8 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 562 us: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (2): json, pprint_safe_repr
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260210-3.15.0a5+-d18dbd5-NOGIL/bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 76.54% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x