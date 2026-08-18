# Results vs. 3.13.0rc2

- fork: python
- ref: a7bb524fef61f77ede01
- machine: darwin-arm64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.041x faster
- HPT reliability: 97.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 346 ms: 1.50x faster                                                    |
| async_generators                 | 193 ms                                                         | 147 ms: 1.31x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 334 ms: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.64x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| nbody          | 42.5 ms                                                        | 42.1 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                   |
| tomli_loads         | 1000 ms                                                        | 851 ms: 1.17x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| json_loads          | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_process   | 25.4 ms                                                        | 26.0 ms: 1.03x slower                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 142 us: 1.09x slower                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 68.7 ms: 1.10x slower                                                   |
| Geometric mean      | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.11 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                   |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 526 ms: 2.01x faster                                                    |
| pylint                           | 106 ms                                                         | 57.3 ms: 1.84x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 317 ms: 1.66x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 346 ms: 1.50x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.18 ms: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 992 ms: 1.47x faster                                                    |
| deepcopy                         | 145 us                                                         | 100 us: 1.45x faster                                                    |
| go                               | 72.6 ms                                                        | 53.3 ms: 1.36x faster                                                   |
| async_generators                 | 193 ms                                                         | 147 ms: 1.31x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 50.3 us: 1.29x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 334 ms: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 187 ms: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 835 us: 1.19x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 851 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 124 ms: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| docutils                         | 1.05 sec                                                       | 964 ms: 1.09x faster                                                    |
| fannkuch                         | 179 ms                                                         | 165 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.5 ms: 1.07x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 116 ms: 1.07x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.7 ms: 1.06x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.88 ms: 1.06x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 176 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.4 ms: 1.05x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 35.5 ms: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.04x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.3 ms: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 922 ns: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.9 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.5 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                    |
| nbody                            | 42.5 ms                                                        | 42.1 ms: 1.01x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                   |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.62 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 315 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.0 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 425 us: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.5 ns: 1.05x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 495 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.11 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.3 ms: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 68.7 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 51.0 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 247 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 267 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.64x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization, logging_format, sphinx, comprehensions, unpickle_pure_python, shortest_path, pprint_pformat
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 97.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x