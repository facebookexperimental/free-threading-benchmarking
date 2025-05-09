# Results vs. 3.13.0rc2

- fork: python
- ref: 6d5a8c2ec19f1c38b455
- machine: darwin-arm64
- commit hash: 6d5a8c2
- commit date: 2025-05-09
- overall geometric mean: 1.026x faster
- HPT reliability: 87.51%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 50.4 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.89 ms: 1.08x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.5 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|---------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 930 ms: 1.07x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| xml_etree_parse     | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| xml_etree_process   | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| xml_etree_generate  | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| json_loads          | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| json_dumps          | 4.65 ms                                                        | 5.14 ms: 1.11x slower                                                   |
| pickle_pure_python  | 130 us                                                         | 144 us: 1.11x slower                                                    |
| Geometric mean      | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.45 ms: 1.02x faster                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.06x faster                                                    |
| mdp                              | 1.06 sec                                                       | 529 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 960 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.27x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.6 ms: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                   |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 913 us: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.89 ms: 1.08x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 930 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.45 ms: 1.02x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 45.1 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                  |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| richards                         | 22.1 ms                                                        | 22.0 ms: 1.01x faster                                                   |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 21.6 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.3 ms: 1.01x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.05 ms: 1.02x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 66.6 us: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 99.4 ms: 1.04x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 492 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 99.5 ms: 1.05x slower                                                   |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.73 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 47.3 ms: 1.08x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.14 ms: 1.11x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.2 ms: 1.11x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.9 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.9 ms: 1.13x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.72 us: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.58 us: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.4 ms: 1.18x slower                                                   |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.32 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 86.2 ms: 2.98x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 194 ns: 4.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (11): fannkuch, pathlib, pprint_safe_repr, coroutines, unpickle_pure_python, telco, json, richards_super, pprint_pformat, sqlite_synth, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-6d5a8c2/bm-20250509-macm4pro-arm64-python-6d5a8c2ec19f1c38b455-3.15.0a0-6d5a8c2.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 87.51% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x