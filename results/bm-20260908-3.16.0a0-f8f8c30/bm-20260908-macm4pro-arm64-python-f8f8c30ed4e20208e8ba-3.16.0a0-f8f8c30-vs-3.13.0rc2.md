# Results vs. 3.13.0rc2

- fork: python
- ref: f8f8c30ed4e20208e8ba
- machine: darwin-arm64
- commit hash: f8f8c30
- commit date: 2026-09-08
- overall geometric mean: 1.058x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 944 ms: 1.11x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| sphinx         | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 313 ms: 1.68x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 339 ms: 1.54x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 313 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 122 ms: 1.17x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.37 ms: 1.14x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 816 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 66.9 ms: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.69 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.61 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 517 ms: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 56.6 ms: 1.87x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 313 ms: 1.68x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 339 ms: 1.54x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                   |
| k_core                           | 1.46 sec                                                       | 979 ms: 1.49x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                   |
| go                               | 72.6 ms                                                        | 52.3 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.8 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.2 ms: 1.30x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 313 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 328 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 816 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 822 us: 1.21x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 122 ms: 1.17x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.41 ms: 1.14x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.37 ms: 1.14x faster                                                   |
| fannkuch                         | 179 ms                                                         | 161 ms: 1.11x faster                                                    |
| docutils                         | 1.05 sec                                                       | 944 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.6 ms: 1.10x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.08x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.08x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.6 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.0 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.6 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.4 ms: 1.05x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 41.1 ms: 1.05x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 625 ms: 1.04x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                   |
| sphinx                           | 409 ms                                                         | 398 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 286 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.39 us: 1.02x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 42.8 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 928 ns: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.66 us: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                   |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                   |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.3 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.61 ms: 1.04x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.07x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.9 ms: 1.07x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.6 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.69 ms: 1.12x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.5 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.0 ms: 1.24x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (4): nbody, thrift, json_loads, xml_etree_generate
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x