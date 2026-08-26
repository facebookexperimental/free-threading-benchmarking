# Results vs. 3.13.0rc2

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: darwin-arm64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.050x faster
- HPT reliability: 99.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.15x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 175 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 127 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.62x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                   |
| nbody          | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                   |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 818 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 99.1 us: 1.00x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.5 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 528 ms: 2.00x faster                                                    |
| pylint                           | 106 ms                                                         | 56.8 ms: 1.86x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 338 ms: 1.54x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                   |
| deepcopy                         | 145 us                                                         | 97.0 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 987 ms: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 53.2 ms: 1.36x faster                                                   |
| async_generators                 | 193 ms                                                         | 145 ms: 1.33x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 49.6 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 818 ms: 1.22x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 335 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 827 us: 1.20x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 123 ms: 1.15x faster                                                    |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.12x faster                                                    |
| docutils                         | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.96 ms: 1.08x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.5 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.0 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 175 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.06x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.92 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.90 ms: 1.06x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 41.6 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.7 ms: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 127 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.7 ms: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.3 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.04x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 927 ns: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| nbody                            | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 643 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 99.1 us: 1.00x faster                                                   |
| connected_components             | 208 ms                                                         | 209 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 424 us: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 319 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.84 ms: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.5 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.63 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.9 ms: 1.15x slower                                                   |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.7 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.2 ms: 1.19x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| many_optionals                   | 200 us                                                         | 243 us: 1.21x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.62x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (5): sphinx, json_loads, logging_format, shortest_path, comprehensions
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 99.59% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x