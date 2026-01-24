# Results vs. 3.13.0rc2

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: darwin-arm64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 385 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.1 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 816 ms: 1.22x faster                                                     |
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.3 ms: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 99.2 us: 1.00x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.51 ms: 1.05x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 218 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.36x faster                                                     |
| mdp                              | 1.06 sec                                                       | 538 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 233 ms: 1.66x faster                                                     |
| k_core                           | 1.46 sec                                                       | 894 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.03 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.9 us: 1.48x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 52.3 ms: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.1 ms: 1.35x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.8 ms: 1.31x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 816 ms: 1.22x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.0 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.4 ms: 1.10x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 905 us: 1.10x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.2 ms: 1.10x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.0 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.98 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 168 ms: 1.07x faster                                                     |
| sphinx                           | 409 ms                                                         | 385 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 619 ms: 1.05x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.51 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.9 us: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.3 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.74 ms: 1.04x faster                                                    |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.34 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.4 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 99.2 us: 1.00x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.0 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 955 ns: 1.01x slower                                                     |
| coverage                         | 31.2 ms                                                        | 31.5 ms: 1.01x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.0 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.07 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.3 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.72 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.5 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.8 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (3): 2to3, logging_silent, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x