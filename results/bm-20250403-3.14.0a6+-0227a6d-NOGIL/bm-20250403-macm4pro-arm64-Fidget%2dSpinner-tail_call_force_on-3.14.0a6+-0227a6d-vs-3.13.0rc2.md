# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tail_call_force_on
- machine: darwin-arm64
- commit hash: 0227a6d
- commit date: 2025-04-03
- overall geometric mean: 1.072x faster
- HPT reliability: 85.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                             |
| docutils       | 1.05 sec                                                       | 984 ms: 1.06x faster                                                             |
| html5lib       | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                            |
| sphinx         | 409 ms                                                         | 404 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 185 ms: 2.82x faster                                                             |
| async_tree_eager_io              | 525 ms                                                         | 197 ms: 2.67x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 188 ms: 2.16x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 201 ms: 1.93x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 82.0 ms: 1.62x faster                                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.55x faster                                                             |
| async_tree_none                  | 142 ms                                                         | 97.6 ms: 1.46x faster                                                            |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.45x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 229 ms: 1.31x faster                                                             |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 8.94 ms: 1.20x faster                                                            |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                             |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                             |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 73.7 ms: 2.55x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.30x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 25.7 ms: 1.22x faster                                                            |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                             |
| nbody          | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                            |
| Geometric mean | (ref)                                                          | 1.01x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                            |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                            |
| regex_compile  | 47.9 ms                                                        | 48.0 ms: 1.00x slower                                                            |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                            |
| tomli_loads          | 1000 ms                                                        | 849 ms: 1.18x faster                                                             |
| xml_etree_parse      | 62.4 ms                                                        | 56.5 ms: 1.10x faster                                                            |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                            |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                            |
| unpickle_pure_python | 99.5 us                                                        | 97.7 us: 1.02x faster                                                            |
| json_dumps           | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                            |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                             |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.51 ms: 1.10x slower                                                            |
| python_startup_no_site | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                            |
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                            |
| mako            | 4.41 ms                                                        | 5.27 ms: 1.19x slower                                                            |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                            |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 185 ms: 2.82x faster                                                             |
| gc_traversal                     | 2.04 ms                                                        | 761 us: 2.68x faster                                                             |
| async_tree_eager_io              | 525 ms                                                         | 197 ms: 2.67x faster                                                             |
| create_gc_cycles                 | 993 us                                                         | 459 us: 2.16x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 188 ms: 2.16x faster                                                             |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 201 ms: 1.93x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 82.0 ms: 1.62x faster                                                            |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.55x faster                                                             |
| k_core                           | 1.46 sec                                                       | 980 ms: 1.49x faster                                                             |
| async_tree_none                  | 142 ms                                                         | 97.6 ms: 1.46x faster                                                            |
| async_tree_memoization           | 184 ms                                                         | 127 ms: 1.45x faster                                                             |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 229 ms: 1.31x faster                                                             |
| go                               | 72.6 ms                                                        | 56.3 ms: 1.29x faster                                                            |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                            |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.9 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                             |
| float                            | 31.4 ms                                                        | 25.7 ms: 1.22x faster                                                            |
| coroutines                       | 10.8 ms                                                        | 8.94 ms: 1.20x faster                                                            |
| scimark_sor                      | 64.0 ms                                                        | 54.1 ms: 1.18x faster                                                            |
| sqlite_synth                     | 948 ns                                                         | 803 ns: 1.18x faster                                                             |
| tomli_loads                      | 1000 ms                                                        | 849 ms: 1.18x faster                                                             |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                             |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                           |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                            |
| async_generators                 | 193 ms                                                         | 172 ms: 1.12x faster                                                             |
| xml_etree_parse                  | 62.4 ms                                                        | 56.5 ms: 1.10x faster                                                            |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                            |
| regex_v8                         | 10.7 ms                                                        | 9.71 ms: 1.10x faster                                                            |
| generators                       | 15.7 ms                                                        | 14.4 ms: 1.09x faster                                                            |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                            |
| pycparser                        | 470 ms                                                         | 437 ms: 1.08x faster                                                             |
| html5lib                         | 23.1 ms                                                        | 21.7 ms: 1.06x faster                                                            |
| docutils                         | 1.05 sec                                                       | 984 ms: 1.06x faster                                                             |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                            |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                             |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                             |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                            |
| unpickle_pure_python             | 99.5 us                                                        | 97.7 us: 1.02x faster                                                            |
| sphinx                           | 409 ms                                                         | 404 ms: 1.01x faster                                                             |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                             |
| regex_compile                    | 47.9 ms                                                        | 48.0 ms: 1.00x slower                                                            |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                             |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                             |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                            |
| pprint_safe_repr                 | 322 ms                                                         | 327 ms: 1.02x slower                                                             |
| richards_super                   | 24.7 ms                                                        | 25.2 ms: 1.02x slower                                                            |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                             |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.02x slower                                                             |
| telco                            | 3.07 ms                                                        | 3.14 ms: 1.03x slower                                                            |
| sympy_integrate                  | 7.53 ms                                                        | 7.80 ms: 1.04x slower                                                            |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                             |
| logging_simple                   | 2.24 us                                                        | 2.34 us: 1.05x slower                                                            |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.4 ms: 1.05x slower                                                            |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                             |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                            |
| typing_runtime_protocols         | 64.6 us                                                        | 68.1 us: 1.05x slower                                                            |
| logging_format                   | 2.45 us                                                        | 2.59 us: 1.06x slower                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 221 ms: 1.06x slower                                                             |
| nqueens                          | 37.2 ms                                                        | 39.7 ms: 1.07x slower                                                            |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.4 ms: 1.07x slower                                                            |
| json_dumps                       | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 46.1 ms: 1.07x slower                                                            |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                             |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                            |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.07x slower                                                             |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.38 ms: 1.08x slower                                                            |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                             |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                             |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                             |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.09x slower                                                            |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                            |
| sympy_sum                        | 52.3 ms                                                        | 57.5 ms: 1.10x slower                                                            |
| python_startup                   | 8.63 ms                                                        | 9.51 ms: 1.10x slower                                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                            |
| meteor_contest                   | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                            |
| chaos                            | 24.3 ms                                                        | 27.3 ms: 1.12x slower                                                            |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                                            |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                            |
| raytrace                         | 109 ms                                                         | 124 ms: 1.14x slower                                                             |
| many_optionals                   | 200 us                                                         | 233 us: 1.16x slower                                                             |
| scimark_lu                       | 42.8 ms                                                        | 49.8 ms: 1.17x slower                                                            |
| comprehensions                   | 6.80 us                                                        | 7.93 us: 1.17x slower                                                            |
| crypto_pyaes                     | 33.6 ms                                                        | 39.3 ms: 1.17x slower                                                            |
| mako                             | 4.41 ms                                                        | 5.27 ms: 1.19x slower                                                            |
| nbody                            | 42.5 ms                                                        | 51.1 ms: 1.20x slower                                                            |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                            |
| coverage                         | 31.2 ms                                                        | 38.4 ms: 1.23x slower                                                            |
| python_startup_no_site           | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                            |
| subparsers                       | 6.26 ms                                                        | 8.27 ms: 1.32x slower                                                            |
| bench_thread_pool                | 412 us                                                         | 572 us: 1.39x slower                                                             |
| async_tree_eager_tg              | 28.9 ms                                                        | 73.7 ms: 2.55x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                                     |

Benchmark hidden because not significant (2): richards, hexiom
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0227a6d-NOGIL/bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 85.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x