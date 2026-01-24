# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: loop_2000
- machine: darwin-arm64
- commit hash: cec96a9
- commit date: 2026-01-24
- overall geometric mean: 1.172x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 109 ms: 1.03x faster                                                    |
| docutils       | 1.05 sec                                                       | 983 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                   |
| sphinx         | 409 ms                                                         | 385 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 215 ms: 2.45x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.89x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 94.7 ms: 1.50x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.3 ms: 1.39x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 36.7 ms: 1.18x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.0 ms: 1.36x faster                                                   |
| nbody          | 42.5 ms                                                        | 39.7 ms: 1.07x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                          | 1.15x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.1 ms: 1.19x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.83 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 669 ms: 1.49x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 75.4 us: 1.32x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 111 us: 1.17x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 21.6 ms: 1.17x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.19x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 8.67 ms: 1.15x faster                                                   |
| mako            | 4.41 ms                                                        | 3.86 ms: 1.14x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 20.0 ms: 1.07x faster                                                   |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 215 ms: 2.45x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                    |
| richards                         | 22.1 ms                                                        | 9.18 ms: 2.40x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 11.1 ms: 2.23x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.89x faster                                                    |
| mdp                              | 1.06 sec                                                       | 591 ms: 1.79x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 222 ms: 1.74x faster                                                    |
| k_core                           | 1.46 sec                                                       | 859 ms: 1.70x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 38.6 ms: 1.66x faster                                                   |
| subparsers                       | 6.26 ms                                                        | 3.81 ms: 1.64x faster                                                   |
| deepcopy                         | 145 us                                                         | 91.5 us: 1.59x faster                                                   |
| go                               | 72.6 ms                                                        | 46.5 ms: 1.56x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 10.6 us: 1.56x faster                                                   |
| scimark_lu                       | 42.8 ms                                                        | 28.0 ms: 1.53x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 94.7 ms: 1.50x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 669 ms: 1.49x faster                                                    |
| pyflate                          | 222 ms                                                         | 150 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 95.3 ms: 1.39x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.38x faster                                                    |
| float                            | 31.4 ms                                                        | 23.0 ms: 1.36x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 974 ns: 1.33x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 75.4 us: 1.32x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.8 ms: 1.31x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.60 ms: 1.29x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 503 ms: 1.29x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.13 ms: 1.29x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 250 ms: 1.28x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 98.2 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.77 sec: 1.20x faster                                                  |
| regex_compile                    | 47.9 ms                                                        | 40.1 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                   |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.59 ms: 1.18x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 36.7 ms: 1.18x faster                                                   |
| pickle_pure_python               | 130 us                                                         | 111 us: 1.17x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 21.6 ms: 1.17x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.17x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 35.0 ns: 1.16x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 8.67 ms: 1.15x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                   |
| mako                             | 4.41 ms                                                        | 3.86 ms: 1.14x faster                                                   |
| chaos                            | 24.3 ms                                                        | 21.6 ms: 1.12x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 39.2 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 898 us: 1.11x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.17 us: 1.10x faster                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 30.7 ms: 1.09x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.83 ms: 1.09x faster                                                   |
| pycparser                        | 470 ms                                                         | 433 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| meteor_contest                   | 47.9 ms                                                        | 44.6 ms: 1.07x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.09 us: 1.07x faster                                                   |
| nbody                            | 42.5 ms                                                        | 39.7 ms: 1.07x faster                                                   |
| logging_format                   | 2.45 us                                                        | 2.29 us: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.07x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 20.0 ms: 1.07x faster                                                   |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.07x faster                                                   |
| docutils                         | 1.05 sec                                                       | 983 ms: 1.06x faster                                                    |
| sphinx                           | 409 ms                                                         | 385 ms: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.5 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                    |
| raytrace                         | 109 ms                                                         | 105 ms: 1.04x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                   |
| 2to3                             | 112 ms                                                         | 109 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 959 ns: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.8 ms: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.68 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.30 ms: 1.06x slower                                                   |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.10x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 58.7 ms: 1.12x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                   |
| pylint                           | 106 ms                                                         | 126 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260124-3.15.0a5+-cec96a9-JIT/bm-20260124-macm4pro-arm64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.172x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.20x