# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.179x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.04x faster                                                            |
| docutils       | 1.05 sec                                                       | 980 ms: 1.07x faster                                                            |
| html5lib       | 23.1 ms                                                        | 19.4 ms: 1.20x faster                                                           |
| sphinx         | 409 ms                                                         | 382 ms: 1.07x faster                                                            |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 215 ms: 2.44x faster                                                            |
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                            |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.90x faster                                                            |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                                            |
| async_tree_none                  | 142 ms                                                         | 95.2 ms: 1.49x faster                                                           |
| async_tree_none_tg               | 133 ms                                                         | 94.5 ms: 1.40x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.40x faster                                                            |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                            |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 37.0 ms: 1.17x faster                                                           |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                            |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                           |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                           |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.5 ms: 1.40x faster                                                           |
| nbody          | 42.5 ms                                                        | 38.9 ms: 1.09x faster                                                           |
| pidigits       | 166 ms                                                         | 155 ms: 1.07x faster                                                            |
| Geometric mean | (ref)                                                          | 1.18x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.4 ms: 1.21x faster                                                           |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                           |
| regex_v8       | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                           |
| regex_dna      | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 71.6 us: 1.39x faster                                                           |
| json_dumps           | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                           |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.1 ms: 1.28x faster                                                           |
| tomli_loads          | 1000 ms                                                        | 788 ms: 1.27x faster                                                            |
| pickle_pure_python   | 130 us                                                         | 110 us: 1.19x faster                                                            |
| xml_etree_process    | 25.4 ms                                                        | 21.6 ms: 1.18x faster                                                           |
| xml_etree_generate   | 35.8 ms                                                        | 30.5 ms: 1.18x faster                                                           |
| xml_etree_parse      | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                           |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                           |
| Geometric mean       | (ref)                                                          | 1.20x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                           |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                           |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|-----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.83 ms: 1.15x faster                                                           |
| genshi_text     | 9.97 ms                                                        | 8.71 ms: 1.15x faster                                                           |
| genshi_xml      | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                           |
| django_template | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                           |
| Geometric mean  | (ref)                                                          | 1.07x faster                                                                    |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 215 ms: 2.44x faster                                                            |
| async_tree_eager_io_tg           | 521 ms                                                         | 215 ms: 2.42x faster                                                            |
| richards                         | 22.1 ms                                                        | 9.44 ms: 2.34x faster                                                           |
| richards_super                   | 24.7 ms                                                        | 11.3 ms: 2.19x faster                                                           |
| async_tree_io_tg                 | 405 ms                                                         | 214 ms: 1.90x faster                                                            |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.85x faster                                                            |
| go                               | 72.6 ms                                                        | 41.7 ms: 1.74x faster                                                           |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                                            |
| k_core                           | 1.46 sec                                                       | 861 ms: 1.70x faster                                                            |
| subparsers                       | 6.26 ms                                                        | 3.76 ms: 1.66x faster                                                           |
| pyflate                          | 222 ms                                                         | 141 ms: 1.58x faster                                                            |
| scimark_sor                      | 64.0 ms                                                        | 41.9 ms: 1.53x faster                                                           |
| deepcopy                         | 145 us                                                         | 96.4 us: 1.50x faster                                                           |
| async_tree_none                  | 142 ms                                                         | 95.2 ms: 1.49x faster                                                           |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                           |
| async_tree_none_tg               | 133 ms                                                         | 94.5 ms: 1.40x faster                                                           |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.40x faster                                                            |
| float                            | 31.4 ms                                                        | 22.5 ms: 1.40x faster                                                           |
| unpickle_pure_python             | 99.5 us                                                        | 71.6 us: 1.39x faster                                                           |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                            |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.3 ms: 1.34x faster                                                           |
| deltablue                        | 1.45 ms                                                        | 1.10 ms: 1.31x faster                                                           |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.30x faster                                                           |
| json_dumps                       | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                           |
| pprint_safe_repr                 | 322 ms                                                         | 251 ms: 1.28x faster                                                            |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.1 ms: 1.28x faster                                                           |
| pprint_pformat                   | 650 ms                                                         | 509 ms: 1.28x faster                                                            |
| tomli_loads                      | 1000 ms                                                        | 788 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                            |
| logging_silent                   | 40.6 ns                                                        | 33.2 ns: 1.22x faster                                                           |
| regex_compile                    | 47.9 ms                                                        | 39.4 ms: 1.21x faster                                                           |
| scimark_fft                      | 124 ms                                                         | 102 ms: 1.21x faster                                                            |
| telco                            | 3.07 ms                                                        | 2.56 ms: 1.20x faster                                                           |
| html5lib                         | 23.1 ms                                                        | 19.4 ms: 1.20x faster                                                           |
| pickle_pure_python               | 130 us                                                         | 110 us: 1.19x faster                                                            |
| fannkuch                         | 179 ms                                                         | 151 ms: 1.19x faster                                                            |
| scimark_lu                       | 42.8 ms                                                        | 36.1 ms: 1.18x faster                                                           |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.81 sec: 1.18x faster                                                          |
| xml_etree_process                | 25.4 ms                                                        | 21.6 ms: 1.18x faster                                                           |
| xml_etree_generate               | 35.8 ms                                                        | 30.5 ms: 1.18x faster                                                           |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                            |
| async_tree_eager                 | 43.2 ms                                                        | 37.0 ms: 1.17x faster                                                           |
| mako                             | 4.41 ms                                                        | 3.83 ms: 1.15x faster                                                           |
| genshi_text                      | 9.97 ms                                                        | 8.71 ms: 1.15x faster                                                           |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                                           |
| chaos                            | 24.3 ms                                                        | 21.4 ms: 1.14x faster                                                           |
| regex_v8                         | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                           |
| create_gc_cycles                 | 993 us                                                         | 885 us: 1.12x faster                                                            |
| crypto_pyaes                     | 33.6 ms                                                        | 30.0 ms: 1.12x faster                                                           |
| comprehensions                   | 6.80 us                                                        | 6.08 us: 1.12x faster                                                           |
| hexiom                           | 2.85 ms                                                        | 2.58 ms: 1.10x faster                                                           |
| pycparser                        | 470 ms                                                         | 430 ms: 1.09x faster                                                            |
| nbody                            | 42.5 ms                                                        | 38.9 ms: 1.09x faster                                                           |
| thrift                           | 309 us                                                         | 284 us: 1.09x faster                                                            |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                            |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                           |
| genshi_xml                       | 21.4 ms                                                        | 19.7 ms: 1.08x faster                                                           |
| json                             | 1.94 ms                                                        | 1.79 ms: 1.08x faster                                                           |
| spectral_norm                    | 43.7 ms                                                        | 40.6 ms: 1.08x faster                                                           |
| meteor_contest                   | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                                           |
| logging_simple                   | 2.24 us                                                        | 2.08 us: 1.07x faster                                                           |
| sphinx                           | 409 ms                                                         | 382 ms: 1.07x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 210 ms: 1.07x faster                                                            |
| pidigits                         | 166 ms                                                         | 155 ms: 1.07x faster                                                            |
| docutils                         | 1.05 sec                                                       | 980 ms: 1.07x faster                                                            |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                            |
| logging_format                   | 2.45 us                                                        | 2.30 us: 1.06x faster                                                           |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                           |
| typing_runtime_protocols         | 64.6 us                                                        | 61.2 us: 1.06x faster                                                           |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                           |
| xml_etree_parse                  | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                           |
| connected_components             | 208 ms                                                         | 198 ms: 1.05x faster                                                            |
| raytrace                         | 109 ms                                                         | 104 ms: 1.05x faster                                                            |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                           |
| 2to3                             | 112 ms                                                         | 107 ms: 1.04x faster                                                            |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                            |
| regex_dna                        | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                                           |
| sympy_integrate                  | 7.53 ms                                                        | 7.45 ms: 1.01x faster                                                           |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                           |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                           |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                           |
| bench_thread_pool                | 412 us                                                         | 426 us: 1.04x slower                                                            |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                           |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                           |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                           |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                            |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                            |
| django_template                  | 12.5 ms                                                        | 13.6 ms: 1.09x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                            |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                            |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                           |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                            |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                           |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                                            |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.9 ms: 2.62x slower                                                           |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                                    |

Benchmark hidden because not significant (2): gc_traversal, sqlite_synth
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260102-3.15.0a3+-8f7b4f4-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.179x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.20x