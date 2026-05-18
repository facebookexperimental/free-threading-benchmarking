# Results vs. 3.13.0rc2

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: darwin-arm64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.048x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 971 ms: 1.08x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 306 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 333 ms: 1.56x faster                                                    |
| async_generators                 | 193 ms                                                         | 147 ms: 1.32x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 45.2 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.5 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 839 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.9 ms: 1.07x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 67.8 ms: 1.09x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.88 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 56.8 ms: 1.86x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 306 ms: 1.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 333 ms: 1.56x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.50x faster                                                   |
| deepcopy                         | 145 us                                                         | 99.9 us: 1.45x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.44x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 147 ms: 1.32x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 49.7 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.30x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 327 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.19x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 839 ms: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 866 us: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.69 ms: 1.10x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.82 ms: 1.09x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| docutils                         | 1.05 sec                                                       | 971 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.9 ms: 1.07x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 278 ms: 1.06x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 175 ms: 1.05x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.0 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.4 ms: 1.05x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.5 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 36.5 ms: 1.02x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 638 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.2 ms: 1.02x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 40.0 ns: 1.01x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 319 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 939 ns: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.3 ms: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.50 ms: 1.00x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.25 us: 1.01x slower                                                   |
| connected_components             | 208 ms                                                         | 211 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 228 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.8 ms: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 488 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.7 ms: 1.05x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.22 us: 1.06x slower                                                   |
| nbody                            | 42.5 ms                                                        | 45.2 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.2 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 67.8 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.88 ms: 1.10x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.0 ms: 1.17x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 40.0 ms: 1.19x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 260 ms: 1.25x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.0 ms: 1.28x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (3): dask, sphinx, logging_format
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260517-3.16.0a0-acefff9/bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x