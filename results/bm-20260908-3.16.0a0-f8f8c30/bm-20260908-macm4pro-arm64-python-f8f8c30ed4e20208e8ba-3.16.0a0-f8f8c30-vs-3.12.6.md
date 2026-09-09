# Results vs. 3.12.6

- fork: python
- ref: f8f8c30ed4e20208e8ba
- machine: darwin-arm64
- commit hash: f8f8c30
- commit date: 2026-09-08
- overall geometric mean: 1.145x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 944 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 313 ms: 1.47x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 122 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 339 ms: 1.32x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 178 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 42.4 ms: 1.28x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.37 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.4 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.6 ms: 1.18x faster                                                   |
| tomli_loads          | 957 ms                                                   | 816 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.9 ms: 1.02x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.21 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.69 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.61 ms: 1.04x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.04x faster                                                   |
| pylint                           | 128 ms                                                   | 56.6 ms: 2.26x faster                                                   |
| mdp                              | 1.09 sec                                                 | 517 ms: 2.11x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.59x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.66 us: 1.48x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 313 ms: 1.47x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 122 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 48.8 us: 1.45x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.41 ms: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.37x faster                                                    |
| go                               | 70.0 ms                                                  | 52.3 ms: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 174 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 339 ms: 1.32x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.1 ms: 1.28x faster                                                   |
| nbody                            | 54.2 ms                                                  | 42.4 ms: 1.28x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.8 ms: 1.27x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 178 ms: 1.25x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.0 ms: 1.24x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.23x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                   |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.6 ms: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 816 ms: 1.17x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 286 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 294 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 979 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.4 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.11x faster                                                   |
| fannkuch                         | 176 ms                                                   | 161 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.0 ms: 1.08x faster                                                   |
| docutils                         | 1.02 sec                                                 | 944 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.41 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.6 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 625 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.3 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 309 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 928 ns: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.3 ms: 1.04x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.61 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.37 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.9 ms: 1.02x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 822 us: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.4 ms: 1.00x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.0 ms: 1.03x slower                                                   |
| 2to3                             | 114 ms                                                   | 119 ms: 1.05x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.21 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.69 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 266 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 245 us: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 154 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (4): bench_thread_pool, json_loads, pickle_pure_python, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.145x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x