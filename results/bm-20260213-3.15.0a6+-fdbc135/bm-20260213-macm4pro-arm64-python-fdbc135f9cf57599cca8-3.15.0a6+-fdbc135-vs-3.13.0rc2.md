# Results vs. 3.13.0rc2

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: darwin-arm64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.4 ms: 1.38x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 844 ms: 1.19x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.9 us: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.85 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                     |
| mdp                              | 1.06 sec                                                       | 529 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 227 ms: 1.78x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 224 ms: 1.72x faster                                                     |
| k_core                           | 1.46 sec                                                       | 895 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.01 ms: 1.56x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.4 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.41x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.4 ms: 1.38x faster                                                    |
| go                               | 72.6 ms                                                        | 53.3 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 137 ms: 1.34x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 249 ms: 1.21x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 844 ms: 1.19x faster                                                     |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.5 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.78 ms: 1.09x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 930 us: 1.07x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 391 ms: 1.04x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.57 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 626 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.3 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.5 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.5 us: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.44 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 98.9 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| connected_components             | 208 ms                                                         | 208 ms: 1.00x slower                                                     |
| 2to3                             | 112 ms                                                         | 112 ms: 1.00x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.3 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.5 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.82 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.85 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.3 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.3 ms: 1.03x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.01 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.8 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.18 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.0 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.38 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.75 ms: 1.08x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.1 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 251 us: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (3): sqlite_synth, thrift, spectral_norm
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260213-3.15.0a6+-fdbc135/bm-20260213-macm4pro-arm64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x