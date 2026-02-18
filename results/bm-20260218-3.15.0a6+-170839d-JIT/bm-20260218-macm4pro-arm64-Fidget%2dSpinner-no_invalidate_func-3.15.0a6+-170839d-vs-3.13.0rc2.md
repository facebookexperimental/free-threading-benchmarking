# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: no_invalidate_func
- machine: darwin-arm64
- commit hash: 170839d
- commit date: 2026-02-18
- overall geometric mean: 1.161x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                             |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                           |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                            |
| sphinx         | 409 ms                                                         | 395 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                          | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.46x faster                                                             |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 219 ms: 1.76x faster                                                             |
| async_tree_none                  | 142 ms                                                         | 94.9 ms: 1.50x faster                                                            |
| async_tree_none_tg               | 133 ms                                                         | 95.0 ms: 1.39x faster                                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                             |
| async_tree_eager                 | 43.2 ms                                                        | 36.9 ms: 1.17x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                             |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                             |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 24.0 ms: 1.31x faster                                                            |
| nbody          | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                            |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.4 ms: 1.18x faster                                                            |
| regex_v8       | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                            |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                            |
| regex_dna      | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 658 ms: 1.52x faster                                                             |
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                            |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                            |
| unpickle_pure_python | 99.5 us                                                        | 84.8 us: 1.17x faster                                                            |
| xml_etree_process    | 25.4 ms                                                        | 21.8 ms: 1.17x faster                                                            |
| xml_etree_generate   | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                            |
| pickle_pure_python   | 130 us                                                         | 126 us: 1.03x faster                                                             |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                            |
| xml_etree_parse      | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.08 ms: 1.05x slower                                                            |
| python_startup_no_site | 5.95 ms                                                        | 6.55 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.95 ms: 1.12x faster                                                            |
| django_template | 12.5 ms                                                        | 13.8 ms: 1.11x slower                                                            |
| Geometric mean  | (ref)                                                          | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.46x faster                                                             |
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                             |
| richards                         | 22.1 ms                                                        | 9.54 ms: 2.31x faster                                                            |
| richards_super                   | 24.7 ms                                                        | 11.3 ms: 2.18x faster                                                            |
| mdp                              | 1.06 sec                                                       | 535 ms: 1.98x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 221 ms: 1.83x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 219 ms: 1.76x faster                                                             |
| subparsers                       | 6.26 ms                                                        | 3.61 ms: 1.74x faster                                                            |
| k_core                           | 1.46 sec                                                       | 865 ms: 1.69x faster                                                             |
| scimark_sor                      | 64.0 ms                                                        | 39.4 ms: 1.62x faster                                                            |
| deepcopy_memo                    | 16.5 us                                                        | 10.4 us: 1.58x faster                                                            |
| deepcopy                         | 145 us                                                         | 94.1 us: 1.54x faster                                                            |
| go                               | 72.6 ms                                                        | 47.8 ms: 1.52x faster                                                            |
| tomli_loads                      | 1000 ms                                                        | 658 ms: 1.52x faster                                                             |
| scimark_lu                       | 42.8 ms                                                        | 28.5 ms: 1.50x faster                                                            |
| async_tree_none                  | 142 ms                                                         | 94.9 ms: 1.50x faster                                                            |
| pyflate                          | 222 ms                                                         | 152 ms: 1.46x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 95.0 ms: 1.39x faster                                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.38x faster                                                             |
| float                            | 31.4 ms                                                        | 24.0 ms: 1.31x faster                                                            |
| deepcopy_reduce                  | 1.30 us                                                        | 994 ns: 1.30x faster                                                             |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                            |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.0 ms: 1.30x faster                                                            |
| pprint_pformat                   | 650 ms                                                         | 510 ms: 1.27x faster                                                             |
| pprint_safe_repr                 | 322 ms                                                         | 254 ms: 1.27x faster                                                             |
| scimark_fft                      | 124 ms                                                         | 97.8 ms: 1.26x faster                                                            |
| deltablue                        | 1.45 ms                                                        | 1.16 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 248 ms: 1.22x faster                                                             |
| regex_compile                    | 47.9 ms                                                        | 40.4 ms: 1.18x faster                                                            |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.1 ms: 1.18x faster                                                            |
| telco                            | 3.07 ms                                                        | 2.60 ms: 1.18x faster                                                            |
| unpickle_pure_python             | 99.5 us                                                        | 84.8 us: 1.17x faster                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 36.9 ms: 1.17x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                             |
| hexiom                           | 2.85 ms                                                        | 2.44 ms: 1.17x faster                                                            |
| xml_etree_process                | 25.4 ms                                                        | 21.8 ms: 1.17x faster                                                            |
| xml_etree_generate               | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                            |
| comprehensions                   | 6.80 us                                                        | 5.86 us: 1.16x faster                                                            |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                             |
| fannkuch                         | 179 ms                                                         | 154 ms: 1.16x faster                                                             |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.16x faster                                                           |
| logging_silent                   | 40.6 ns                                                        | 35.3 ns: 1.15x faster                                                            |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                            |
| mako                             | 4.41 ms                                                        | 3.95 ms: 1.12x faster                                                            |
| spectral_norm                    | 43.7 ms                                                        | 39.2 ms: 1.12x faster                                                            |
| regex_v8                         | 10.7 ms                                                        | 9.76 ms: 1.10x faster                                                            |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                            |
| nqueens                          | 37.2 ms                                                        | 34.4 ms: 1.08x faster                                                            |
| chaos                            | 24.3 ms                                                        | 22.5 ms: 1.08x faster                                                            |
| pycparser                        | 470 ms                                                         | 438 ms: 1.07x faster                                                             |
| create_gc_cycles                 | 993 us                                                         | 932 us: 1.07x faster                                                             |
| connected_components             | 208 ms                                                         | 196 ms: 1.06x faster                                                             |
| nbody                            | 42.5 ms                                                        | 40.0 ms: 1.06x faster                                                            |
| crypto_pyaes                     | 33.6 ms                                                        | 31.9 ms: 1.05x faster                                                            |
| async_generators                 | 193 ms                                                         | 184 ms: 1.05x faster                                                             |
| shortest_path                    | 225 ms                                                         | 214 ms: 1.05x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                            |
| meteor_contest                   | 47.9 ms                                                        | 45.8 ms: 1.05x faster                                                            |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                            |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                             |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                            |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                            |
| sphinx                           | 409 ms                                                         | 395 ms: 1.03x faster                                                             |
| pickle_pure_python               | 130 us                                                         | 126 us: 1.03x faster                                                             |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                             |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                             |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                            |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                           |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                            |
| typing_runtime_protocols         | 64.6 us                                                        | 64.0 us: 1.01x faster                                                            |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                             |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                             |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                             |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.03x slower                                                            |
| xml_etree_parse                  | 62.4 ms                                                        | 64.1 ms: 1.03x slower                                                            |
| sympy_str                        | 95.5 ms                                                        | 98.3 ms: 1.03x slower                                                            |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                             |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                            |
| regex_dna                        | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                            |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                             |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.04x slower                                                             |
| sympy_sum                        | 52.3 ms                                                        | 54.7 ms: 1.05x slower                                                            |
| python_startup                   | 8.63 ms                                                        | 9.08 ms: 1.05x slower                                                            |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                            |
| python_startup_no_site           | 5.95 ms                                                        | 6.55 ms: 1.10x slower                                                            |
| django_template                  | 12.5 ms                                                        | 13.8 ms: 1.11x slower                                                            |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                             |
| many_optionals                   | 200 us                                                         | 237 us: 1.18x slower                                                             |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.6 ms: 2.72x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                                     |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-170839d-JIT/bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.161x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.23x