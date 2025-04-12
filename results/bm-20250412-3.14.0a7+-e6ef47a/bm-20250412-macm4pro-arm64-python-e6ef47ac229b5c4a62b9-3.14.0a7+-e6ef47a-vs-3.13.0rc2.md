# Results vs. 3.13.0rc2

- fork: python
- ref: e6ef47ac229b5c4a62b9
- machine: darwin-arm64
- commit hash: e6ef47a
- commit date: 2025-04-12
- overall geometric mean: 1.039x faster
- HPT reliability: 94.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.4 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 895 ms: 1.12x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                    |
| json_loads          | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| json_dumps          | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 143 us: 1.10x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.97 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.73 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 239 ms: 2.20x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                     |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 246 ms: 1.65x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| k_core                           | 1.46 sec                                                       | 940 ms: 1.56x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| go                               | 72.6 ms                                                        | 56.2 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.29x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 257 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 879 us: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 895 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.97 ms: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.05x faster                                                     |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.9 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 41.8 ms: 1.03x faster                                                    |
| 2to3                             | 112 ms                                                         | 108 ms: 1.03x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 47.1 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.6 us: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 40.3 ns: 1.01x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.3 ms: 1.00x faster                                                    |
| richards                         | 22.1 ms                                                        | 22.1 ms: 1.00x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.7 ms: 1.01x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 24.9 ms: 1.01x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 655 ms: 1.01x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 98.5 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 485 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 165 ms: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.97 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 45.5 ms: 1.04x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.7 ms: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.36 us: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.58 us: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.31 ms: 1.06x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.3 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.97 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.94 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.11x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.6 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.5 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.73 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                     |
| nbody                            | 42.5 ms                                                        | 48.4 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.58 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (10): sphinx, genshi_text, sqlite_synth, genshi_xml, nqueens, xml_etree_generate, unpickle_pure_python, fannkuch, pprint_safe_repr, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250412-3.14.0a7+-e6ef47a/bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7+-e6ef47a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 94.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x