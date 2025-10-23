# Results vs. 3.13.0rc2

- fork: python
- ref: bd2c7e8c8b10f4d31eab
- machine: darwin-arm64
- commit hash: bd2c7e8
- commit date: 2025-10-22
- overall geometric mean: 1.005x faster
- HPT reliability: 57.36%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 231 ms: 2.25x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 44.4 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.6 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 51.6 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 974 ms: 1.03x faster                                                     |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| mako            | 4.41 ms                                                        | 5.05 ms: 1.14x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 231 ms: 2.25x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| mdp                              | 1.06 sec                                                       | 547 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 231 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 907 ms: 1.61x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| deepcopy                         | 145 us                                                         | 113 us: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 60.3 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.1 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.87 ms: 1.08x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 926 us: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.06 sec: 1.04x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 974 ms: 1.03x faster                                                     |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.60 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.4 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.8 ms: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 420 us: 1.02x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.6 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 44.4 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 25.5 ms: 1.03x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.2 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 981 ns: 1.04x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 2.95 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.85 ms: 1.04x slower                                                    |
| thrift                           | 309 us                                                         | 321 us: 1.04x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 67.2 us: 1.04x slower                                                    |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.1 ms: 1.05x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.6 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 341 ms: 1.06x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 691 ms: 1.06x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.4 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.3 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.2 ms: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 105 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.7 ms: 1.10x slower                                                    |
| fannkuch                         | 179 ms                                                         | 197 ms: 1.10x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.7 ms: 1.10x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 178 ms: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| raytrace                         | 109 ms                                                         | 123 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.76 us: 1.14x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.05 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.16x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                     |
| nbody                            | 42.5 ms                                                        | 51.6 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 370 us: 1.85x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 18.1 ms: 2.90x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.6 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (5): dask, sphinx, regex_dna, docutils, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 57.36% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.16x