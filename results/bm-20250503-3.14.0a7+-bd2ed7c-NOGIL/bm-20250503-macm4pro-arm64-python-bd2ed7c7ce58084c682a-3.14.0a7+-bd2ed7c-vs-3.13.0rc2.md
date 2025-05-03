# Results vs. 3.13.0rc2

- fork: python
- ref: bd2ed7c7ce58084c682a
- machine: darwin-arm64
- commit hash: bd2ed7c
- commit date: 2025-05-03
- overall geometric mean: 1.013x faster
- HPT reliability: 68.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| html5lib       | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                    |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.2 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 35.5 ms: 1.30x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 55.2 ms: 1.13x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 974 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.28 ms: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| json_loads           | 10.8 us                                                        | 12.6 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.33 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.79 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 746 us: 2.74x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 449 us: 2.21x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.06x faster                                                     |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.2 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 35.5 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.21x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| deepcopy                         | 145 us                                                         | 126 us: 1.15x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                    |
| go                               | 72.6 ms                                                        | 63.4 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 832 ns: 1.14x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 55.2 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 28.2 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 974 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.1 ms: 1.00x faster                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                     |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                     |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                    |
| json                             | 1.94 ms                                                        | 2.06 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.33 ms: 1.08x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.32 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                     |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.9 ns: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 357 ms: 1.11x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 25.7 ms: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.1 ms: 1.13x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.28 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.79 ms: 1.14x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.77 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.16x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.16x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 74.9 us: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 50.4 ms: 1.17x slower                                                    |
| json_loads                       | 10.8 us                                                        | 12.6 us: 1.17x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.89 us: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.9 ms: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.1 ms: 1.25x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.86 us: 1.30x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 57.4 ms: 1.34x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 585 us: 1.42x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.56 ms: 1.53x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.6 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250503-3.14.0a7+-bd2ed7c-NOGIL/bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7+-bd2ed7c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 68.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x