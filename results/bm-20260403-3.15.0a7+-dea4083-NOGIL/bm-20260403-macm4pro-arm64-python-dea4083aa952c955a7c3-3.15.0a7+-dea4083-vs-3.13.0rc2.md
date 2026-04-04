# Results vs. 3.13.0rc2

- fork: python
- ref: dea4083aa952c955a7c3
- machine: darwin-arm64
- commit hash: dea4083
- commit date: 2026-04-03
- overall geometric mean: 1.015x faster
- HPT reliability: 52.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| sphinx         | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.7 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 863 ms: 1.16x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.82 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.1 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 807 us: 2.53x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 242 ms: 2.15x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 505 us: 1.97x faster                                                     |
| mdp                              | 1.06 sec                                                       | 602 ms: 1.76x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.13 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 60.1 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 787 ns: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.87 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 863 ms: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.5 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.4 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 422 ms: 1.03x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.4 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.0 ns: 1.08x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.66 us: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.8 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 341 us: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.11x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.1 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.5 ms: 1.13x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.82 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.14 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.9 ms: 1.24x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.46 us: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.60 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.27x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 56.6 ms: 1.32x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.6 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 269 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.35x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 566 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.7 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260403-3.15.0a7+-dea4083-NOGIL/bm-20260403-macm4pro-arm64-python-dea4083aa952c955a7c3-3.15.0a7+-dea4083.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 52.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x