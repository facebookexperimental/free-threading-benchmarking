# Results vs. 3.13.0rc2

- fork: python
- ref: e56f86fb6cc7cf14c255
- machine: darwin-arm64
- commit hash: e56f86f
- commit date: 2026-09-04
- overall geometric mean: 1.022x slower
- HPT reliability: 95.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 131 ms: 1.18x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 446 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 296 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 294 ms: 1.77x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 295 ms: 1.37x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                    |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 303 ms: 1.03x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 237 ms: 1.05x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (2): async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 63.4 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 916 ms: 1.09x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.56 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.32x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 786 us: 2.60x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 493 us: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 54.5 ms: 1.94x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 296 ms: 1.78x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 294 ms: 1.77x faster                                                    |
| mdp                              | 1.06 sec                                                       | 607 ms: 1.74x faster                                                    |
| k_core                           | 1.46 sec                                                       | 999 ms: 1.47x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.34 ms: 1.44x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 295 ms: 1.37x faster                                                    |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 306 ms: 1.26x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                   |
| async_generators                 | 193 ms                                                         | 157 ms: 1.23x faster                                                    |
| go                               | 72.6 ms                                                        | 60.8 ms: 1.19x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 798 ns: 1.19x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 14.1 us: 1.16x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 56.6 us: 1.14x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.90 sec: 1.12x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 58.0 ms: 1.10x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 916 ms: 1.09x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.23 us: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 180 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.02x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| pycparser                        | 470 ms                                                         | 481 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 303 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 139 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 237 ms: 1.05x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                   |
| sphinx                           | 409 ms                                                         | 446 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.48 us: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 721 ms: 1.11x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.5 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                   |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 49.1 ms: 1.12x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.13x slower                                                   |
| thrift                           | 309 us                                                         | 351 us: 1.14x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.1 ms: 1.14x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.6 ms: 1.14x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.4 ms: 1.14x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 29.4 ms: 1.16x slower                                                   |
| connected_components             | 208 ms                                                         | 242 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| chaos                            | 24.3 ms                                                        | 28.5 ms: 1.17x slower                                                   |
| 2to3                             | 112 ms                                                         | 131 ms: 1.18x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.19x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.21 us: 1.21x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 49.4 ns: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 41.4 ms: 1.23x slower                                                   |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.56 ms: 1.27x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.86 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.70 ms: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.0 ms: 1.32x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 63.4 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 269 us: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 556 us: 1.35x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 63.2 ms: 1.48x slower                                                   |
| generators                       | 15.7 ms                                                        | 23.7 ms: 1.51x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 163 ms: 1.59x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (3): async_tree_none, pidigits, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260904-3.16.0a0-e56f86f-NOGIL/bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 95.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x