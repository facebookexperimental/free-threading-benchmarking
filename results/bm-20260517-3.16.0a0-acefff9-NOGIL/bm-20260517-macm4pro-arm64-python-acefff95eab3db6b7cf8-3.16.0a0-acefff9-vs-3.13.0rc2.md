# Results vs. 3.13.0rc2

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: darwin-arm64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.021x faster
- HPT reliability: 51.68%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.89x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 279 ms: 1.88x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 273 ms: 1.49x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.43x faster                                                    |
| async_generators                 | 193 ms                                                         | 151 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 171 ms: 1.09x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 132 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.07x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 127 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.3 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| float          | 31.4 ms                                                        | 32.8 ms: 1.04x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.5 ms: 1.12x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.26x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 802 us: 2.55x faster                                                    |
| pylint                           | 106 ms                                                         | 53.3 ms: 1.98x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 508 us: 1.96x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.89x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 279 ms: 1.88x faster                                                    |
| mdp                              | 1.06 sec                                                       | 588 ms: 1.80x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.20 ms: 1.49x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 273 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.43x faster                                                    |
| deepcopy                         | 145 us                                                         | 105 us: 1.38x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                   |
| async_generators                 | 193 ms                                                         | 151 ms: 1.28x faster                                                    |
| go                               | 72.6 ms                                                        | 58.5 ms: 1.24x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 790 ns: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.14 ms: 1.17x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 857 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 55.5 us: 1.16x faster                                                   |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 56.5 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 171 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 132 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 58.2 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 282 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 127 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                    |
| pycparser                        | 470 ms                                                         | 459 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.00x slower                                                  |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.4 ns: 1.04x slower                                                   |
| float                            | 31.4 ms                                                        | 32.8 ms: 1.04x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 682 ms: 1.05x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.3 ms: 1.05x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 38.0 ms: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.01 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 51.5 ms: 1.07x slower                                                   |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.4 ms: 1.08x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.9 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.1 ms: 1.12x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 28.5 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                   |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.07 us: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| coverage                         | 31.2 ms                                                        | 38.2 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                    |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                   |
| generators                       | 15.7 ms                                                        | 20.7 ms: 1.32x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.4 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 573 us: 1.39x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.0 ms: 1.43x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 111 ms: 3.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): html5lib, json_loads
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 51.68% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x