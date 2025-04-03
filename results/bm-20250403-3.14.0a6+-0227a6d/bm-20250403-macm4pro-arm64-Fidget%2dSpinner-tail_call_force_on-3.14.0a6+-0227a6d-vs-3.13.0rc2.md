# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tail_call_force_on
- machine: darwin-arm64
- commit hash: 0227a6d
- commit date: 2025-04-03
- overall geometric mean: 1.066x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 106 ms: 1.05x faster                                                             |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                           |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.24x faster                                                             |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                             |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                             |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                             |
| async_generators                 | 193 ms                                                         | 166 ms: 1.17x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 9.29 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                             |
| async_tree_eager                 | 43.2 ms                                                        | 39.1 ms: 1.10x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                             |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                             |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.5 ms: 2.96x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                            |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                             |
| nbody          | 42.5 ms                                                        | 46.8 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                          | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                            |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                            |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                            |
| regex_dna      | 94.6 ms                                                        | 104 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 801 ms: 1.25x faster                                                             |
| xml_etree_generate   | 35.8 ms                                                        | 33.0 ms: 1.08x faster                                                            |
| unpickle_pure_python | 99.5 us                                                        | 92.7 us: 1.07x faster                                                            |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                            |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                            |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                            |
| pickle_pure_python   | 130 us                                                         | 134 us: 1.03x slower                                                             |
| json_dumps           | 4.65 ms                                                        | 4.95 ms: 1.06x slower                                                            |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                            |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                            |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 19.3 ms: 1.10x faster                                                            |
| genshi_text     | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                            |
| mako            | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                            |
| django_template | 12.5 ms                                                        | 14.2 ms: 1.14x slower                                                            |
| Geometric mean  | (ref)                                                          | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.24x faster                                                             |
| async_tree_eager_io_tg           | 521 ms                                                         | 248 ms: 2.10x faster                                                             |
| mdp                              | 1.06 sec                                                       | 505 ms: 2.10x faster                                                             |
| async_tree_io_tg                 | 405 ms                                                         | 242 ms: 1.67x faster                                                             |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                             |
| k_core                           | 1.46 sec                                                       | 945 ms: 1.55x faster                                                             |
| deepcopy                         | 145 us                                                         | 98.1 us: 1.48x faster                                                            |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                            |
| go                               | 72.6 ms                                                        | 51.3 ms: 1.41x faster                                                            |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                             |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                             |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                             |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                             |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                            |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                            |
| tomli_loads                      | 1000 ms                                                        | 801 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                             |
| dulwich_log                      | 19.8 ms                                                        | 17.0 ms: 1.17x faster                                                            |
| async_generators                 | 193 ms                                                         | 166 ms: 1.17x faster                                                             |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                             |
| coroutines                       | 10.8 ms                                                        | 9.29 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                             |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                             |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                           |
| generators                       | 15.7 ms                                                        | 14.0 ms: 1.12x faster                                                            |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                            |
| regex_compile                    | 47.9 ms                                                        | 43.3 ms: 1.11x faster                                                            |
| create_gc_cycles                 | 993 us                                                         | 898 us: 1.11x faster                                                             |
| genshi_xml                       | 21.4 ms                                                        | 19.3 ms: 1.10x faster                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 39.1 ms: 1.10x faster                                                            |
| hexiom                           | 2.85 ms                                                        | 2.59 ms: 1.10x faster                                                            |
| xml_etree_generate               | 35.8 ms                                                        | 33.0 ms: 1.08x faster                                                            |
| genshi_text                      | 9.97 ms                                                        | 9.23 ms: 1.08x faster                                                            |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                            |
| logging_silent                   | 40.6 ns                                                        | 37.8 ns: 1.07x faster                                                            |
| unpickle_pure_python             | 99.5 us                                                        | 92.7 us: 1.07x faster                                                            |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                            |
| typing_runtime_protocols         | 64.6 us                                                        | 60.7 us: 1.07x faster                                                            |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.3 ms: 1.07x faster                                                            |
| pprint_pformat                   | 650 ms                                                         | 610 ms: 1.06x faster                                                             |
| richards_super                   | 24.7 ms                                                        | 23.2 ms: 1.06x faster                                                            |
| pprint_safe_repr                 | 322 ms                                                         | 304 ms: 1.06x faster                                                             |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                            |
| 2to3                             | 112 ms                                                         | 106 ms: 1.05x faster                                                             |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.04x faster                                                            |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                            |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                             |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                             |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                            |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                             |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                            |
| sqlalchemy_declarative           | 44.4 ms                                                        | 43.1 ms: 1.03x faster                                                            |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                            |
| sqlite_synth                     | 948 ns                                                         | 923 ns: 1.03x faster                                                             |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                            |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                             |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.01x faster                                                            |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                           |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                            |
| meteor_contest                   | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                             |
| sympy_str                        | 95.5 ms                                                        | 94.9 ms: 1.01x faster                                                            |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.01x faster                                                             |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                             |
| bench_thread_pool                | 412 us                                                         | 414 us: 1.01x slower                                                             |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.08 ms: 1.02x slower                                                            |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                            |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                             |
| pickle_pure_python               | 130 us                                                         | 134 us: 1.03x slower                                                             |
| sympy_sum                        | 52.3 ms                                                        | 53.9 ms: 1.03x slower                                                            |
| comprehensions                   | 6.80 us                                                        | 7.04 us: 1.04x slower                                                            |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                            |
| coverage                         | 31.2 ms                                                        | 32.5 ms: 1.04x slower                                                            |
| python_startup                   | 8.63 ms                                                        | 9.05 ms: 1.05x slower                                                            |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                             |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                             |
| mako                             | 4.41 ms                                                        | 4.65 ms: 1.05x slower                                                            |
| json_dumps                       | 4.65 ms                                                        | 4.95 ms: 1.06x slower                                                            |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                            |
| nqueens                          | 37.2 ms                                                        | 39.9 ms: 1.07x slower                                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 40.5 ms: 1.07x slower                                                            |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                            |
| regex_dna                        | 94.6 ms                                                        | 104 ms: 1.10x slower                                                             |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                            |
| nbody                            | 42.5 ms                                                        | 46.8 ms: 1.10x slower                                                            |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                            |
| many_optionals                   | 200 us                                                         | 225 us: 1.12x slower                                                             |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                            |
| spectral_norm                    | 43.7 ms                                                        | 49.6 ms: 1.13x slower                                                            |
| django_template                  | 12.5 ms                                                        | 14.2 ms: 1.14x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                             |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.26x slower                                                             |
| subparsers                       | 6.26 ms                                                        | 8.28 ms: 1.32x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.5 ms: 2.96x slower                                                            |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                                     |

Benchmark hidden because not significant (4): logging_format, pycparser, json, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0227a6d/bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.07x