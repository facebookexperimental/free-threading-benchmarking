# Results vs. 3.13.0rc2

- fork: python
- ref: ae7fc4a4f6b711173bb7
- machine: darwin-arm64
- commit hash: ae7fc4a
- commit date: 2026-02-23
- overall geometric mean: 1.071x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 397 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.9 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.88 ms: 1.09x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.7 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps          | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| xml_etree_iterparse | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                    |
| tomli_loads         | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| xml_etree_generate  | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process   | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| pickle_pure_python  | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.13 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.57 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 235 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 230 ms: 1.68x faster                                                     |
| k_core                           | 1.46 sec                                                       | 903 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.06 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.2 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.38x faster                                                     |
| go                               | 72.6 ms                                                        | 52.8 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 98.9 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 138 ms: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.1 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| pyflate                          | 222 ms                                                         | 189 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.5 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.5 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.88 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.06x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 946 us: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 397 ms: 1.03x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.5 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 316 ms: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.8 us: 1.01x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 643 ms: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.00x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.02x slower                                                    |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 43.6 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.02 us: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 98.3 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.05x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.13 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.76 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.57 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.10x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.2 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 257 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.7 ms: 2.79x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (8): json, pycparser, thrift, sympy_integrate, unpickle_pure_python, logging_silent, json_loads, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260223-3.15.0a6+-ae7fc4a/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x