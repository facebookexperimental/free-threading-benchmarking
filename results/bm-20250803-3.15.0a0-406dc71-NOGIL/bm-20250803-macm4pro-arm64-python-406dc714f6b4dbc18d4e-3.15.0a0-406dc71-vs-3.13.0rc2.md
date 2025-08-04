# Results vs. 3.13.0rc2

- fork: python
- ref: 406dc714f6b4dbc18d4e
- machine: darwin-arm64
- commit hash: 406dc71
- commit date: 2025-08-03
- overall geometric mean: 1.008x faster
- HPT reliability: 66.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.1 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100.0 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.00x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.3 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 196 ms: 2.66x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 778 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 205 ms: 2.56x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.1 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100.0 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| go                               | 72.6 ms                                                        | 60.3 ms: 1.20x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 819 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.8 ms: 1.15x faster                                                   |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 972 ms: 1.03x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.55 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pycparser                        | 470 ms                                                         | 467 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.8 ms: 1.00x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.4 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.19 ms: 1.04x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.5 ms: 1.04x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 220 ms: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.4 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.02 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 348 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 710 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.4 ns: 1.09x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.59 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.3 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.5 ms: 1.12x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.52 us: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.1 us: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.8 ms: 1.17x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.18 us: 1.20x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.3 ms: 1.23x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.4 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.28x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.5 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 58.9 ms: 1.39x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 599 us: 1.45x slower                                                    |
| many_optionals                   | 200 us                                                         | 334 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.94x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (4): async_tree_eager_cpu_io_mixed, sphinx, json, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 66.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x