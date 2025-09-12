# Results vs. 3.13.0rc2

- fork: python
- ref: f96f7c9f5b5db35e8a22
- machine: darwin-arm64
- commit hash: f96f7c9
- commit date: 2025-09-11
- overall geometric mean: 1.001x faster
- HPT reliability: 76.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.8 ms: 1.16x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| mako            | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 474 us: 2.10x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 607 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.6 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.48x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 235 ms: 1.28x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 62.1 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.04 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 830 ns: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                   |
| pyflate                          | 222 ms                                                         | 204 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                   |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 996 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 981 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                   |
| pycparser                        | 470 ms                                                         | 478 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.4 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.07 ms: 1.07x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.11x slower                                                    |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.58 ms: 1.11x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.6 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 361 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.9 ns: 1.13x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.13x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 737 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 43.0 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.1 ms: 1.14x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.1 us: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.8 ms: 1.16x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.3 ms: 1.17x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.6 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.19x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.44 us: 1.24x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.5 ms: 1.24x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.9 ms: 1.28x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.31 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.87 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 58.0 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 579 us: 1.41x slower                                                    |
| many_optionals                   | 200 us                                                         | 333 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.95x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250911-3.15.0a0-f96f7c9-NOGIL/bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 76.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x