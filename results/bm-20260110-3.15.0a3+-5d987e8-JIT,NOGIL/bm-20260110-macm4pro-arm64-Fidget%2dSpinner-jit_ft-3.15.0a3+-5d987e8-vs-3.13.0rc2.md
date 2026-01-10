# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.103x faster
- HPT reliability: 99.74%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                 |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                               |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                          | 1.01x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                 |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                 |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                 |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                 |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                 |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                 |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                 |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                 |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                 |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                |
| async_generators                 | 193 ms                                                         | 200 ms: 1.03x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                 |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.6 ms: 3.17x slower                                                |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                         |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 21.6 ms: 1.45x faster                                                |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                 |
| nbody          | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                          | 1.12x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                |
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                |
| regex_compile  | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                |
| regex_dna      | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                          | 1.08x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 739 ms: 1.35x faster                                                 |
| unpickle_pure_python | 99.5 us                                                        | 76.8 us: 1.30x faster                                                |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                |
| json_dumps           | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                |
| pickle_pure_python   | 130 us                                                         | 113 us: 1.15x faster                                                 |
| xml_etree_generate   | 35.8 ms                                                        | 32.3 ms: 1.11x faster                                                |
| xml_etree_process    | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                          | 1.16x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.93 ms: 1.15x slower                                                |
| python_startup_no_site | 5.95 ms                                                        | 7.12 ms: 1.20x slower                                                |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                |
| genshi_xml      | 21.4 ms                                                        | 27.4 ms: 1.28x slower                                                |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 819 us: 2.49x faster                                                 |
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                 |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                 |
| richards                         | 22.1 ms                                                        | 10.4 ms: 2.13x faster                                                |
| richards_super                   | 24.7 ms                                                        | 12.6 ms: 1.95x faster                                                |
| create_gc_cycles                 | 993 us                                                         | 519 us: 1.92x faster                                                 |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                 |
| subparsers                       | 6.26 ms                                                        | 3.78 ms: 1.66x faster                                                |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                 |
| mdp                              | 1.06 sec                                                       | 664 ms: 1.59x faster                                                 |
| go                               | 72.6 ms                                                        | 46.1 ms: 1.57x faster                                                |
| k_core                           | 1.46 sec                                                       | 948 ms: 1.54x faster                                                 |
| pyflate                          | 222 ms                                                         | 145 ms: 1.53x faster                                                 |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                |
| float                            | 31.4 ms                                                        | 21.6 ms: 1.45x faster                                                |
| scimark_sor                      | 64.0 ms                                                        | 44.5 ms: 1.44x faster                                                |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.40x faster                                                |
| tomli_loads                      | 1000 ms                                                        | 739 ms: 1.35x faster                                                 |
| async_tree_memoization_tg        | 186 ms                                                         | 142 ms: 1.31x faster                                                 |
| unpickle_pure_python             | 99.5 us                                                        | 76.8 us: 1.30x faster                                                |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                 |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.28x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                 |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.8 ms: 1.25x faster                                                |
| json_dumps                       | 4.65 ms                                                        | 3.72 ms: 1.25x faster                                                |
| fannkuch                         | 179 ms                                                         | 143 ms: 1.25x faster                                                 |
| logging_silent                   | 40.6 ns                                                        | 32.6 ns: 1.24x faster                                                |
| deltablue                        | 1.45 ms                                                        | 1.17 ms: 1.24x faster                                                |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.78 sec: 1.20x faster                                               |
| scimark_monte_carlo              | 29.9 ms                                                        | 25.0 ms: 1.20x faster                                                |
| pprint_safe_repr                 | 322 ms                                                         | 271 ms: 1.19x faster                                                 |
| pprint_pformat                   | 650 ms                                                         | 556 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 258 ms: 1.17x faster                                                 |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                 |
| pickle_pure_python               | 130 us                                                         | 113 us: 1.15x faster                                                 |
| scimark_fft                      | 124 ms                                                         | 109 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                 |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                |
| xml_etree_generate               | 35.8 ms                                                        | 32.3 ms: 1.11x faster                                                |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                 |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                |
| regex_compile                    | 47.9 ms                                                        | 44.3 ms: 1.08x faster                                                |
| xml_etree_process                | 25.4 ms                                                        | 23.5 ms: 1.08x faster                                                |
| pycparser                        | 470 ms                                                         | 436 ms: 1.08x faster                                                 |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                |
| scimark_lu                       | 42.8 ms                                                        | 40.8 ms: 1.05x faster                                                |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                               |
| async_tree_eager                 | 43.2 ms                                                        | 41.4 ms: 1.04x faster                                                |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                 |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                |
| chaos                            | 24.3 ms                                                        | 23.9 ms: 1.02x faster                                                |
| json                             | 1.94 ms                                                        | 1.93 ms: 1.01x faster                                                |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                 |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                 |
| regex_dna                        | 94.6 ms                                                        | 96.0 ms: 1.01x slower                                                |
| comprehensions                   | 6.80 us                                                        | 6.92 us: 1.02x slower                                                |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                 |
| crypto_pyaes                     | 33.6 ms                                                        | 34.4 ms: 1.02x slower                                                |
| nbody                            | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                |
| async_generators                 | 193 ms                                                         | 200 ms: 1.03x slower                                                 |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                |
| meteor_contest                   | 47.9 ms                                                        | 49.8 ms: 1.04x slower                                                |
| logging_simple                   | 2.24 us                                                        | 2.33 us: 1.04x slower                                                |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.05x slower                                                |
| typing_runtime_protocols         | 64.6 us                                                        | 68.8 us: 1.06x slower                                                |
| raytrace                         | 109 ms                                                         | 117 ms: 1.07x slower                                                 |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                 |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                 |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                |
| shortest_path                    | 225 ms                                                         | 245 ms: 1.09x slower                                                 |
| connected_components             | 208 ms                                                         | 233 ms: 1.12x slower                                                 |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                |
| python_startup                   | 8.63 ms                                                        | 9.93 ms: 1.15x slower                                                |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                 |
| sympy_sum                        | 52.3 ms                                                        | 62.2 ms: 1.19x slower                                                |
| pylint                           | 106 ms                                                         | 126 ms: 1.19x slower                                                 |
| sympy_str                        | 95.5 ms                                                        | 114 ms: 1.20x slower                                                 |
| python_startup_no_site           | 5.95 ms                                                        | 7.12 ms: 1.20x slower                                                |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 251 ms: 1.21x slower                                                 |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                |
| bench_mp_pool                    | 37.8 ms                                                        | 47.2 ms: 1.25x slower                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                 |
| genshi_xml                       | 21.4 ms                                                        | 27.4 ms: 1.28x slower                                                |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                 |
| generators                       | 15.7 ms                                                        | 21.0 ms: 1.33x slower                                                |
| bench_thread_pool                | 412 us                                                         | 564 us: 1.37x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.6 ms: 3.17x slower                                                |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                         |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260110-3.15.0a3+-5d987e8-JIT,NOGIL/bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 99.74% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.33x