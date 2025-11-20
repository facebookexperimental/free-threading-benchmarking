# Results vs. 3.13.0rc2

- fork: python
- ref: ca1e86f9d963dc298d9a
- machine: darwin-arm64
- commit hash: ca1e86f
- commit date: 2025-11-19
- overall geometric mean: 1.040x faster
- HPT reliability: 99.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.8 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| nbody          | 42.5 ms                                                        | 46.2 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 861 ms: 1.16x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.7 us: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 142 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.99 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 226 ms: 2.31x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 228 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 542 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 228 ms: 1.70x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                     |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 54.1 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 141 ms: 1.31x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 26.7 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 861 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.77 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.06x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.2 ms: 1.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 941 us: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.1 ms: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                     |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 46.9 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 97.7 us: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.80 ms: 1.02x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 642 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 320 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.7 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.2 ms: 1.02x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.50 us: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.6 ns: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 973 ns: 1.03x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| dask                             | 525 ms                                                         | 542 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.11 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.99 ms: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.16 us: 1.05x slower                                                    |
| pylint                           | 106 ms                                                         | 111 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.9 ms: 1.06x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.8 ms: 1.07x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.7 ms: 1.08x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.08x slower                                                     |
| nbody                            | 42.5 ms                                                        | 46.2 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 142 us: 1.09x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 44.7 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.23x slower                                                     |
| many_optionals                   | 200 us                                                         | 363 us: 1.81x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.8 ms: 2.83x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.87x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (7): pycparser, spectral_norm, typing_runtime_protocols, genshi_text, async_tree_eager_cpu_io_mixed, thrift, json
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251119-3.15.0a2+-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2+-ca1e86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 99.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x